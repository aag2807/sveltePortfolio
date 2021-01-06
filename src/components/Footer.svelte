<script>
  import { Footer, Button } from "svelte-materialify/src";
  import { link } from "svelte-spa-router";

  import Divider from "../utils/Divider.svelte";

  const links = [
    {path:"/", to:"Home"},
    {path:"/contact", to:"Contact"},
    {path:"/projects", to:"Project"},
  ];

</script>

<style lang="scss">
  $primary: #222831;
  $secondary: #393e46;
  $info: #edf6f9;
  $light: #ffddd2;
  $dark: #e29578;
  $text-light: #eeeeee;
  $text-dark: #d65a31;

  div {
    color: $text-light;
  }

  a{
    text-decoration: none;
    transition: color .70s;

    &:visited{
      text-decoration: none;
    }
    &:hover{
      color: $text-dark;
    }

  }
</style>

<Divider />

<Footer
  padless
  class="justify-center flex-column"
  style="background-color: #222831;">
  <div class="mt-2 mb-2">
    {#each links as linke (linke)}
      <Button text rounded><a href={linke.path} use:link>{linke.to}</a></Button>
    {/each}
  </div>
  <div class="lighten-1 pa-2 text-center" style="width:100%;">
    2021 -
    <b>Alvaro Guzman</b>
  </div>
</Footer>
