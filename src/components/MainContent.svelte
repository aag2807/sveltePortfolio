<script>
import Divider from "../utils/Divider.svelte";

</script>

<style>
  /* block-$ */
  .block-effect {
    font-size: calc(8px + 5vw);
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


</style>



<div style='align-text:center;'>
  <h1 class="block-effect" style="--td: 1.2s">
    <div class="block-reveal" style="--bc: #393e46; --d: .1s">
      “Imagination is more 
    </div>
    <div class="block-reveal" style="--bc: #673ab7; --d: .5s">
      important than knowledge."
    </div>
  </h1>
</div>

<Divider />