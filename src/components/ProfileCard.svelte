<script>
  import { Icon } from "svelte-materialify/src";
</script>

<div class="container1">
  <div class="row">
    <div class="column">
      <div class="img">
        <img src="/images/avatar.png" alt="" />
      </div>
    </div>
    <div class="column">
      <h4 class="white-text text-h3 mt-4 mr-3">
        Alvaro <br />
        Guzman
      </h4>
    </div>
  </div>
  <div class="row" style="height:70px;">
    <div class="column ">
      <div class="box">
        <a href="/Alvaro_cv.pdf" target="_blank" class="link">
          <Icon size="24px" class="far fa-file" />
          <span style="font-size: 0.75rem;
          ">cv</span>
        </a>
      </div>
    </div>
    <div class="column">
      <div class="box">
        <a href="https://www.github.com/aag2807" target="_blank" class="link">
          <Icon class="fab fa-github" />
        </a>
      </div>
    </div>
    <div class="column ">
      <div class="box">
        <a href="https://www.instagram.com/red_2807/" target="_blank" class="link">
          <Icon class="fab fa-instagram" />
        </a>
      </div>
    </div>
  </div>
</div>

<style lang="scss">
  $primary: #222831;
  $secondary: #393e46;
  $info: #edf6f9;
  $light: #ffddd2;
  $dark: #e29578;
  $text-light: #eeeeee;
  $text-dark: #d65a31;

  .row {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    width: 100%;
  }

  .column {
    display: flex;
    flex-direction: column;
    flex-basis: 100%;
    flex: 1;
  }

  .box {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .container1 {
    padding: 0 auto;
    height: 220px;
    width: 320px;
    max-width: 100%;
    margin-bottom: 1.25rem;
    background-color: $primary;

    border: 1px solid $secondary;
    border-radius: 25px;
    text-align: center;

    a {
      padding: 10px 20px;
      border: 2px solid $text-light;
      border-radius: 9px;
      width: 100px;

      color: $text-light;
      text-decoration: none;
      background: transparent;

      font-size: 1.2rem;
      transition: border 0.7s ease, background-color 0.7s ease,
        color 0.7s ease-in;

      &:hover {
        border: 2px solid $text-dark;
        background-color: $text-dark;
        color: $primary;
      }
    }
  }

  img {
    margin-top: 1.5rem;
    margin-left: 0.85rem;
    width: 85px;
    max-width: 100px;
    border-radius: 50%;
    transition: width 0.8s, transform 0.7s ease;

    &:hover {
      transform: translate(-35%, -40%);
      cursor: pointer;
      width: 100px;
    }
  }
</style>
