<script>
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

  import Divider from "../utils/Divider.svelte";
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
    max-width: 100%;
  }

  .mb {
    display: none;
  }

  .dt{
    display: block;
  }

  @media screen and (max-width: 600px) {
    .mb {
      display: block;
    }

    .dt{
      display: none;
    }

  }
</style>

<!-- 
  svelte: amber darken-4
  vue: green darken-4
  react:  light-blue darken-4
  angular: red darken-4
  vanilla: yellow accent-2

  -->
<div class="mb">
  <h3 class='text-h3 text-center'>Projects</h3>
    <Col>
      <Card class="blue-grey darken-4 grey-text text-lighten-5">
        <Row>
          <Col class="ml-2">
            <CardTitle>Insta-Vue</CardTitle>
            <CardSubtitle />
            <CardActions>
              <Button outlined class="green">More</Button>
            </CardActions>
          </Col>
          <Col>
            <p>A minimalistic Instagram clone</p>
            <p>
              made with:<br />
              <Chip class="green lighten-2">Vue</Chip>
              <Chip class="red lighten-1">Firebase</Chip>
              <Chip class="green">Quasar</Chip>
            </p>
          </Col>
        </Row>
      </Card>
    
      <Divider />
    
      <Card class="blue-grey darken-4 grey-text text-lighten-5">
        <Row>
          <Col class="ml-2">
            <CardTitle>Vanilla.js SPA</CardTitle>
            <CardSubtitle />
            <CardActions>
              <Button
                outlined
                style="font-family: inherit;"
                class="yellow accent-5">
                More
              </Button>
            </CardActions>
          </Col>
          <Col>
            <p>A frameworkless SPA</p>
            <p>
              made with:<br />
              <Chip class="orange darken-2">Jquery</Chip>
              <Chip class="amber darken-1">Handlebars</Chip>
            </p>
          </Col>
        </Row>
      </Card>
    
      <Divider />
    
      <Card class="blue-grey darken-4 grey-text text-lighten-5">
        <Row>
          <Col class="ml-2">
            <CardTitle>E-commerce React</CardTitle>
            <CardSubtitle />
            <CardActions>
              <Button
                outlined
                style="font-family: inherit;"
                class="light-blue darken-4">
                More
              </Button>
            </CardActions>
          </Col>
          <Col>
            <p>React Slack Chat clone</p>
            <p>
              made with:<br />
              <Chip class="light-blue darken-1">React</Chip>
              <Chip class="light-blue darken-3">CommerceJs</Chip>
              <Chip class="grey darken-2">Material Ui React</Chip>
            </p>
          </Col>
        </Row>
      </Card>
    
      <Divider />
    
      <Card class="blue-grey darken-4 grey-text text-lighten-5">
        <Row>
          <Col class="ml-2">
            <CardTitle>Rack Chat</CardTitle>
            <CardSubtitle />
            <CardActions>
              <Button
                outlined
                style="font-family: inherit;"
                class="light-blue darken-4">
                More
              </Button>
            </CardActions>
          </Col>
          <Col>
            <p>React Slack Chat clone</p>
            <p>
              made with:<br />
              <Chip class="red lighten-1">Firebase</Chip>
              <Chip class="light-blue darken-1">React</Chip>
              <Chip class="grey lighten-1">Semantic Ui React</Chip>
            </p>
          </Col>
        </Row>
      </Card>
    
      <Divider />
    
      <Card class="blue-grey darken-4 grey-text text-lighten-5">
        <Row>
          <Col class="ml-2">
            <CardTitle>Svelte<br> Portfolio</CardTitle>
            <CardSubtitle />
            <CardActions>
              <Button outlined class="yellow darken-4">More</Button>
            </CardActions>
          </Col>
          <Col>
            <p>A minimalistic Whatsapp clone</p>
            <p>
              made with:<br />
              <Chip class="green lighten-2">Vue</Chip>
              <Chip class="red lighten-1">Firebase</Chip>
              <Chip class="green">Quasar</Chip>
            </p>
          </Col>
        </Row>
      </Card>
      <Divider />
    </Col> 
</div>

<div class="dt">
  <Row>
    <Col>
      <h3 class='text-h3 text-center'>Front-End</h3>
      <Divider />
      <Card class="blue-grey darken-4 grey-text text-lighten-5">
        <Row>
          <Col class="ml-2">
            <CardTitle>Insta-Vue</CardTitle>
            <CardSubtitle />
            <CardActions>
              <Button outlined class="green">More</Button>
            </CardActions>
          </Col>
          <Col>
            <p>A minimalistic Instagram clone</p>
            <p>
              made with:<br />
              <Chip class="green lighten-2">Vue</Chip>
              <Chip class="red lighten-1">Firebase</Chip>
              <Chip class="green">Quasar</Chip>
            </p>
          </Col>
        </Row>
      </Card>
    
      <Divider />
    
      <Card class="blue-grey darken-4 grey-text text-lighten-5">
        <Row>
          <Col class="ml-2">
            <CardTitle>Vanilla.js SPA</CardTitle>
            <CardSubtitle />
            <CardActions>
              <Button
                outlined
                style="font-family: inherit;"
                class="yellow accent-5">
                More
              </Button>
            </CardActions>
          </Col>
          <Col>
            <p>A frameworkless SPA</p>
            <p>
              made with:<br />
              <Chip class="orange darken-2">Jquery</Chip>
              <Chip class="amber darken-1">Handlebars</Chip>
            </p>
          </Col>
        </Row>
      </Card>
    
      <Divider />
    
      <Card class="blue-grey darken-4 grey-text text-lighten-5">
        <Row>
          <Col class="ml-2">
            <CardTitle>E-commerce React</CardTitle>
            <CardSubtitle />
            <CardActions>
              <Button
                outlined
                style="font-family: inherit;"
                class="light-blue darken-4">
                More
              </Button>
            </CardActions>
          </Col>
          <Col>
            <p>React Slack Chat clone</p>
            <p>
              made with:<br />
              <Chip class="light-blue darken-1">React</Chip>
              <Chip class="light-blue darken-3">CommerceJs</Chip>
              <Chip class="grey darken-2">Material Ui React</Chip>
            </p>
          </Col>
        </Row>
      </Card>
    
      <Divider />
    
      <Card class="blue-grey darken-4 grey-text text-lighten-5">
        <Row>
          <Col class="ml-2">
            <CardTitle>Rack Chat</CardTitle>
            <CardSubtitle />
            <CardActions>
              <Button
                outlined
                style="font-family: inherit;"
                class="light-blue darken-4">
                More
              </Button>
            </CardActions>
          </Col>
          <Col>
            <p>React Slack Chat clone</p>
            <p>
              made with:<br />
              <Chip class="red lighten-1">Firebase</Chip>
              <Chip class="light-blue darken-1">React</Chip>
              <Chip class="grey lighten-1">Semantic Ui React</Chip>
            </p>
          </Col>
        </Row>
      </Card>
    
      <Divider />
    
      <Card class="blue-grey darken-4 grey-text text-lighten-5">
        <Row>
          <Col class="ml-2">
            <CardTitle>Vue-C</CardTitle>
            <CardSubtitle />
            <CardActions>
              <Button outlined class="green">More</Button>
            </CardActions>
          </Col>
          <Col>
            <p>A minimalistic Whatsapp clone</p>
            <p>
              made with:<br />
              <Chip class="green lighten-2">Vue</Chip>
              <Chip class="red lighten-1">Firebase</Chip>
              <Chip class="green">Quasar</Chip>
            </p>
          </Col>
        </Row>
      </Card>
      <Divider />
      <Card class="blue-grey darken-4 grey-text text-lighten-5">
        <Row>
          <Col class="ml-2">
            <CardTitle>Svelte<br> Portfolio</CardTitle>
            <CardSubtitle />
            <CardActions>
              <Button outlined class="yellow darken-4">More</Button>
            </CardActions>
          </Col>
          <Col>
            <p>A minimalistic Whatsapp clone</p>
            <p>
              made with:<br />
              <Chip class="green lighten-2">Vue</Chip>
              <Chip class="red lighten-1">Firebase</Chip>
              <Chip class="green">Quasar</Chip>
            </p>
          </Col>
        </Row>
      </Card>
    </Col> 
    <Col>
      <h3 class='text-h3 text-center'>Back-End</h3>
      <Divider />
      <Card class="blue-grey darken-4 grey-text text-lighten-5">
        <Row>
          <Col class="ml-2">
            <CardTitle>Golang-Api's</CardTitle>
            <CardSubtitle />
            <CardActions>
              <Button outlined class="blue lighten-2">More</Button>
            </CardActions>
          </Col>
          <Col>
            <p>Microservices and api's created with:</p>
            <p>
              <br />
              <Chip class="blue lighten-2">Golang</Chip>
              <Chip class="yellow darken-3">beevo</Chip>
              <Chip class="blue-grey">gin</Chip>
              <Chip class="blue-grey darken-2">Mux</Chip>
            </p>
          </Col>
        </Row>
      </Card>
    
      <Divider />
    
      <Card class="blue-grey darken-4 grey-text text-lighten-5">
        <Row>
          <Col class="ml-2">
            <CardTitle>Nest Js Api</CardTitle>
            <CardSubtitle />
            <CardActions>
              <Button
                outlined
                style="font-family: inherit;"
                class="red darken-2">
                More
              </Button>
            </CardActions>
          </Col>
          <Col>
            <p>Where do you think this is coming from?</p>
            <p>
              <Chip class="red darken-2">Nest.js</Chip>
              <Chip class="blue darken-1">Typescript</Chip>
            </p>
          </Col>
        </Row>
      </Card>
    
      <Divider />
    
      <Card class="blue-grey darken-4 grey-text text-lighten-5">
        <Row>
          <Col class="ml-2">
            <CardTitle>MERN template</CardTitle>
            <CardSubtitle />
            <CardActions>
              <Button
                outlined
                style="font-family: inherit;"
                class="light-blue accent-2">
                More
              </Button>
            </CardActions>
          </Col>
          <Col>
            <p>A Use ready template for Mern apps</p>
            <p>
              made with:<br />
              <Chip class="green accent-4">Mongo</Chip>
              <Chip class="yellow darken-3">Express</Chip>
              <Chip class="green darken-2">Node</Chip>
            </p>
          </Col>
        </Row>
      </Card>
    
      <Divider />
    
      <Card class="blue-grey darken-4 grey-text text-lighten-5">
        <Row>
          <Col class="ml-2">
            <CardTitle>Haskell Api</CardTitle>
            <CardSubtitle />
            <CardActions>
              <Button
                outlined
                style="font-family: inherit;"
                class="light-blue darken-4">
                More
              </Button>
            </CardActions>
          </Col>
          <Col>
            <p>React Slack Chat clone</p>
            <p>
              made with:<br />
              <Chip class="red lighten-1">Firebase</Chip>
              <Chip class="light-blue darken-1">React</Chip>
              <Chip class="grey lighten-1">Semantic Ui React</Chip>
            </p>
          </Col>
        </Row>
      </Card>
    
      <Divider />
    
      <Card class="blue-grey darken-4 grey-text text-lighten-5">
        <Row>
          <Col class="ml-2">
            <CardTitle>Rust microservice</CardTitle>
            <CardSubtitle />
            <CardActions>
              <Button outlined class="green">More</Button>
            </CardActions>
          </Col>
          <Col>
            <p>A minimalistic Whatsapp clone</p>
            <p>
              made with:<br />
              <Chip class="green lighten-2">Vue</Chip>
              <Chip class="red lighten-1">Firebase</Chip>
              <Chip class="green">Quasar</Chip>
            </p>
          </Col>
        </Row>
      </Card>
      <Divider />

      <Card class="blue-grey darken-4 grey-text text-lighten-5">
        <Row>
          <Col class="ml-2">
            <CardTitle>RoR microservice</CardTitle>
            <CardSubtitle />
            <CardActions>
              <Button outlined class="green">More</Button>
            </CardActions>
          </Col>
          <Col>
            <p>A minimalistic Whatsapp clone</p>
            <p>
              made with:<br />
              <Chip class="green lighten-2">Vue</Chip>
              <Chip class="red lighten-1">Firebase</Chip>
              <Chip class="green">Quasar</Chip>
            </p>
          </Col>
        </Row>
      </Card>
    </Col> 
  </Row>
</div>