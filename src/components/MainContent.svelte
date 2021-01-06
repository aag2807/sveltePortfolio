<script>
  // your script goes here
</script>

<style>
  .box{
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;
    max-width: 100%;
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
  }
</style>

<!-- markup (zero or more items) goes here -->
<div class='box'>
  <div class="cols a">s</div>
  <div class="cols b">d</div>
</div>