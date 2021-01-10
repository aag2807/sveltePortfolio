<script>
  import { Card, CardText, CardActions, Button } from "svelte-materialify/src";
  import {link} from 'svelte-spa-router'

  //props
  export let overline = "overline";
  export let headline = "title";
  export let content = "content";
  export let btnContent = "Click";
  export let url = "/";
</script>

<style>
  .btn-box {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }
</style>

<div class="d-flex justify-center mt-4 mb-4">
  <Card hover flat outlined style="max-width:300px; min-width:150px;">
    <div class="pl-4 pr-4 pt-3 text-center">
      <span class="text-overline"> {overline} </span>
      <br />
      <span class="text-h5 mb-2">{headline}</span>
      <br />
    </div>
    <CardText class="text-center">{@html content}</CardText>
    <div class="btn-box">
      <CardActions style='width:100%;'>
        <Button class="orange-text text-darken-4" depressed block >
          <!-- svelte-ignore a11y-missing-attribute -->
          <a use:link={url}>{btnContent}</a>
        </Button>
      </CardActions>
    </div>
  </Card>
</div>
