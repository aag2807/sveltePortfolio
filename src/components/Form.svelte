<script>
  import {
    Row,
    Col,
    TextField,
    Textarea,
    Button,
    Container
  } from "svelte-materialify/src";
</script>

<style lang="scss">
  $primary: #222831;
  $secondary: #393e46;
  $info: #edf6f9;
  $light: #ffddd2;
  $dark: #e29578;
  $text-light: #eeeeee;
  $text-dark: #d65a31;

  .f-box {
    background-color: $secondary;
    color: $text-light;
    width: 100%;
    height: 100%;
    border-radius: 8px;
    border: 1px solid $primary;
    border-top: 4px solid $text-dark;
    border-radius: 8px;
  }

  .div {
    margin-bottom: 1rem;
  }
</style>

<div class="f-box">
  <form on:submit|preventDefault>
    <div class="div" />
    <Container>
      <Row>
        <Col>
          <TextField solo color="#eeeeee">First Name</TextField>
        </Col>
        <Col>
          <TextField solo color="#eeeeee">Last Name</TextField>
        </Col>
      </Row>
      <Row>
        <Col>
          <TextField solo color="#eeeeee">Email</TextField>
          <div class="div" />
          <Textarea solo color="#eeeeee">Message</Textarea>
        </Col>
      </Row>
      <Row>
        <Col>
          <Button block class="orange-text text-darken-4">Clear</Button>
        </Col>
        <Col>
          <Button block class="orange-text text-darken-4">Send</Button>
        </Col>
      </Row>
    </Container>
  </form>
</div>
