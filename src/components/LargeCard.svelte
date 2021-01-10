<script lang="ts">
  import { fade } from "svelte/transition";
  import { linear } from "svelte/easing";

  import { Card, CardText, CardActions, Button } from 'svelte-materialify/src';
  import axios from "axios";
  import { onMount } from "svelte";
  import Loader from "../utils/Loader.svelte";

  interface IAbout {
    id?: string | number;
    title: string;
    content: string;
    overlay: string;
  }

  let info:IAbout[] = [];
  let loading = true;
  let error = false;
  let clicked = false

  onMount(async () => {
    try {
      const { data } = await axios.get("http://localhost:3000/about");
      info = data;
      loading = false;
    } catch (e) {
      console.error(e.message())
      loading = true;
    }
  });

  const hideCard =() => clicked = !clicked

  $: hidden = clicked ? 'none' : '';

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
  $card-color: #040505;
  $line-height: 15px;

  .box {
    max-width: 100%;
    width: 100%;
    height: 100%;
    border-radius: 10px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    color: $text-light;
  }

  .card-text {
    padding: 0 5%;
  }

  .card1 {
    background-color: $card-color;
    opacity: 0.4;
    box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
    backdrop-filter: blur(4px);
    -webkit-backdrop-filter: blur(4px);
    border-radius: 10px;
    border: 1px solid rgba(255, 255, 255, 0.18);
    height: 300px;
    width: 300px;
    margin: 5px;
    transition: transform 1s, background-color 1s, opacity 1s;
    display: flex;
    flex-direction: column;

    .card-title {
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: center;
      margin-top: 5%;
    }

    .line {
      height: 2px;
      width: 100%;
      background-color: $text-light;
      margin-top: $line-height;
      opacity: 0.8;
      transition: opacity 0.75s;

      &:hover {
        opacity: 1;
      }
    }

    &:hover {
      transform: translate(-15%, -20%);
      opacity: 0.75;
      background-color: #000;
      cursor: pointer;
    }
  }

  .card2 {
    background: $card-color;
    opacity: 0.4;
    box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
    backdrop-filter: blur(6px);
    -webkit-backdrop-filter: blur(6px);
    border-radius: 10px;
    border: 1px solid rgba(255, 255, 255, 0.18);
    height: 300px;
    width: 300px;
    margin: 5px;
    transition: transform 1s, background-color 1s, opacity 1s;
    display: flex;
    flex-direction: column;

    .card-title {
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: center;
      margin-top: 5%;
    }

    .line {
      height: 2px;
      width: 100%;
      background-color: $text-light;
      margin-top: $line-height;
      opacity: 0.8;
      transition: opacity 0.75s;

      &:hover {
        opacity: 1;
      }
    }

    &:hover {
      transform: translateY(-20%);
      opacity: 0.75;
      background-color: #000;
      cursor: pointer;
    }
  }

  .card3 {
    background: $card-color;
    opacity: 0.4;
    box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
    backdrop-filter: blur(6px);
    -webkit-backdrop-filter: blur(6px);
    border-radius: 10px;
    border: 1px solid rgba(255, 255, 255, 0.18);
    height: 300px;
    width: 300px;
    margin: 5px;
    transition: transform 1s, background-color 1s, opacity 1s;
    display: flex;
    flex-direction: column;

    .card-title {
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: center;
      margin-top: 5%;
    }

    .line {
      height: 2px;
      width: 100%;
      background-color: $text-light;
      margin-top: $line-height;
      opacity: 0.8;
      transition: opacity 0.75s;

      &:hover {
        opacity: 1;
      }
    }

    &:hover {
      transform: translate(15%, -20%);
      opacity: 0.75;
      background-color: #000;
      cursor: pointer;
    }
  }

  @media screen and (max-width: 600px) {
    .box {
      flex-direction: column;
    }

    .card1 {
      margin-bottom: 25px;
      height: 325px;
    }

    .card2 {
      height: 325px;
      margin-bottom: 25px;
    }

    .card2 {
      margin-bottom: 25px;
      height: 325px;
    }
    .card3:hover {
      transform: translateY(-16%);
    }

    .card2:hover {
      transform: translateY(-16%);
    }

    .card1:hover {
      transform: translateY(-16%);
    }
  }
</style>

{#if loading}
  <Loader />
{:else if error && !loading || error && loading}
  <div transition:fade={options}>
    <div class="d-flex justify-center mt-4 mb-4"  style="display:{hidden}">
      <Card outlined style="max-width:300px; color: white;" class='deep-purple lighten-2 text-center'>  
        <div class="pl-4 pr-4 pt-3">
          <br />
          <span class="text-h4 mb-2">ERROR</span>
          <br />
        </div>
        <CardText class='text-center'>
          Seems there was an issue with the backend.
        </CardText >
          <CardActions>
            <Button class='' rounded outlined on:click={hideCard} >OK</Button>
          </CardActions>
      </Card>
    </div>
  </div>
{:else}
  <div class="box">
    {#each info as data (data.id)}
      <div class="card{data.id}">
        <div class="text-subtitle-1 text-center text-decoration-underline sub">
          {data.overlay}
        </div>
        <div class="card-title">
          <h3 class="text-h3 text-center">{data.title}</h3>
        </div>
        <div class="card-text text-center text-caption">
          {@html data.content}
          <div class="line" />
        </div>
      </div>
    {/each}
  </div>
{/if}
