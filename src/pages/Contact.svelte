<script>
  import { fade } from "svelte/transition";
  import { linear } from "svelte/easing";
  import Form from "../components/Form.svelte";

  const options = { duration: 1000, easing: linear };
</script>

<style lang="scss">
  $primary: #222831;
  $secondary: #393e46;
  $info: #edf6f9;
  $light: #ffddd2;
  $dark: #e29578;
  $text-light: #eeeeee;
  $text-dark: #d65a31;

  img {
    max-width: 400px;
    width: 300px;
  }

  .p {
    color: $text-dark;
  }

  .flex {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }
</style>

<!-- markup (zero or more items) goes here -->
<div transition:fade={options}>
  <div class="container flex">
    <img src="images/student-colour-800px.png" alt="" />
    <h4 class="text-h4 text-center">Pitch <span class="p">me</span> an Idea</h4>
  </div>
  <div class="text-center">
    <div class="subtitle-1">I would love to hear from you.</div>
  </div>
  <Form />
</div>
