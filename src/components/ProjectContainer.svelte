<script>
  import axios from "axios";
  import { onMount } from "svelte";
  import { fade } from "svelte/transition";
  import { linear } from "svelte/easing";
  import {
    Chip,
    Button,
    Card,
    Col,
    Row,
    CardTitle,
    CardActions,
    CardSubtitle,
    Icon,
  } from "svelte-materialify";

  import Loader from "../utils/Loader.svelte";
  import Divider from "../utils/Divider.svelte";

  let frontend = [];
  let backend = [];

  async function getFront() {
    const { data } = await axios.get("https://intense-ravine-59043.herokuapp.com/projects/front");
    frontend = [...data];
  }

  async function getBack() {
    const { data } = await axios.get("https://intense-ravine-59043.herokuapp.com/projects/back");
    backend = [...data];
  }

  onMount(async () => {
    await getFront();
    await getBack();
  });

  $: empty = backend.length == 0 && frontend.length == 0;

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



  a {
    text-decoration: none;

    &:link {
      text-decoration: none;
    }

    &:visited {
      text-decoration: none;
    }
  }

  .mb {
    display: none;
  }

  .dt {
    display: block;
  }

  @media screen and (max-width: 600px) {
    .mb {
      display: block;
    }

    .dt {
      display: none;
    }
  }
</style>

{#if empty}
  <Loader />
{:else}
  <div class="mb" transition:fade={options}>
    <h3 class="text-h3 text-center">Projects</h3>
    {#each frontend as front (front.id)}
      <Card class="blue-grey darken-4 grey-text text-lighten-5">
        <Row>
          <Col class="ml-2">
            <CardTitle>
              {@html front.title}
            </CardTitle>
            <CardActions>
              <Button outlined class={front.btnColor}>
                <!-- svelte-ignore a11y-invalid-attribute -->
                <a href="#"> More </a>
              </Button>
            </CardActions>
          </Col>
          <Col>
            {@html front.subtitle}
            <p class="text-subtitle-2">
              {#each front.chips as chip}
                <Chip class={chip.colors}>{chip.title}</Chip>
              {/each}
            </p>
          </Col>
        </Row>
      </Card>

      <Divider />
    {/each}
  </div>

  <div transition:fade={options} class="dt">
    <Row>
      <Col>
        <h3 class="text-h3 text-center">Front-End</h3>

        <Divider />
        {#each frontend as front (front.id)}
          <Card class="blue-grey darken-4 grey-text text-lighten-5">
            <Row>
              <Col class="ml-2">
                <CardTitle>
                  {@html front.title}
                </CardTitle>
                <CardActions>
                  <Button outlined class={front.btnColor}>
                    <!-- svelte-ignore a11y-invalid-attribute -->
                    <a target="_blank" href="#"> More </a>
                  </Button>
                </CardActions>
              </Col>
              <Col>
                {@html front.subtitle}
                <p class="text-subtitle-2">
                  {#each front.chips as chip}
                    <Chip class={chip.colors}>{chip.title}</Chip>
                  {/each}
                </p>
              </Col>
            </Row>
          </Card>

          <Divider />
        {/each}
      </Col>

      <Col>
        <h3 class="text-h3 text-center">Back-End</h3>

        <Divider />

        {#each backend as back (back.id)}
          <Card class="blue-grey darken-4 grey-text text-lighten-5">
            <Row>
              <Col class="ml-2">
                <CardTitle>
                  {@html back.title}
                </CardTitle>
                <CardActions>
                  <Button outlined class={back.btnColor}>
                    <!-- svelte-ignore a11y-invalid-attribute -->
                    <a target="_blank" href="#"> More </a>
                  </Button>
                </CardActions>
              </Col>
              <Col>
                {@html back.subtitle}
                <p class="text-subtitle-2">
                  {#each back.chips as chip}
                    <Chip class={chip.colors}>{chip.title}</Chip>
                  {/each}
                </p>
              </Col>
            </Row>
          </Card>
          <Divider />
        {/each}
      </Col>
    </Row>
  </div>
{/if}
