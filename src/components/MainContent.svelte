<script>
  // your script goes here

import Divider from "../utils/Divider.svelte";

</script>

<style>
  /* .box{
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;
    max-width: 100%;
    padding: 1rem;
    margin: 1rem;
  }
  .cols{
    max-width: 100%;
    width: 50%;
    height: 100px;
  }
  .a {
    background-color: aqua;
  }
  .b {
    background-color: yellow;
  }

  @media screen and (max-width: 600px) {
    .cols {
      width: 100%;
    }
  } */

  /* reset */
  *,
  *::before,
  *::after {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;

    min-height: 100vh;
    padding: 20px;

    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  }

  /* other */
  .info {
    margin: 20px 0;
    text-align: center;
  }

  p {
    color: #2e2e2e;
    margin-bottom: 20px;
  }

  /* block-$ */
  .block-effect {
    font-size: calc(8px + 6vw);
  }

  .block-reveal {
    --t: calc(var(--td) + var(--d));

    color: transparent;
    padding: 4px;

    position: relative;
    overflow: hidden;

    animation: revealBlock 0s var(--t) forwards;
  }

  .block-reveal::after {
    content: "";

    width: 0%;
    height: 100%;
    padding-bottom: 4px;

    position: absolute;
    top: 0;
    left: 0;

    background: var(--bc);
    animation: revealingIn var(--td) var(--d) forwards,
      revealingOut var(--td) var(--t) forwards;
  }

  /* animations */
  @keyframes revealBlock {
    100% {
      color: #0f0f0f;
    }
  }

  @keyframes revealingIn {
    0% {
      width: 0;
    }

    100% {
      width: 100%;
    }
  }

  @keyframes revealingOut {
    0% {
      transform: translateX(0);
    }

    100% {
      transform: translateX(100%);
    }
  }

  .abs-site-link {
    position: fixed;
    bottom: 20px;
    left: 20px;
    color: hsla(0, 0%, 0%, 0.6);
    font-size: 16px;
  }

</style>

<!-- markup (zero or more items) goes here -->
<!-- <div class='box'>
  <div class="cols a">

  </div>
  <div class="cols b">

  </div>
</div> -->

<div style='align-text:center;'>
  <h1 class="block-effect" style="--td: 1.2s">
    <div class="block-reveal" style="--bc: #4040bf; --d: .1s">
      “Imagination is more 
    </div>
    <div class="block-reveal" style="--bc: #bf4060; --d: .5s">
      import than knowledge."
    </div>
  </h1>
</div>

<Divider />