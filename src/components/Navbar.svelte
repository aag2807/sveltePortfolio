<script>
  import {link} from 'svelte-spa-router'
</script>

<!-- svelte-ignore component-name-lowercase -->
<style lang="scss">
  $primary: #222831;
  $secondary: #393e46;
  $info: #edf6f9;
  $light: #ffddd2;
  $dark: #e29578;
  $text-light: #eeeeee;
  $text-dark: #d65a31;

  .containers {
    width: 100%;
    display: inline-block;
  }

  /** HEADER */

  /** NAVIGATION BAR */
  nav {
    overflow: hidden;
    background-color: $primary;
    top: 0;
    width: 100%;
    ul {
      text-align: center;
      list-style-type: none;
      list-style-type: none;
      margin: 0;
      padding: 15px;
      li {
        display: inline;
        font-family: "Fira Sans", sans-serif;
        font-size: 17px;
        a {
          color: $text-light;
          text-decoration: none;
          padding: 14px;
          transition: background 1s, color 1s;
          &:hover {
            background-color: $secondary;
            color: $text-dark;
          }
        }
      }
    }
  }
</style>

<!-- markup (zero or more items) goes here -->
<svelte:head>
  <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.15.1/css/all.css" integrity="sha384-vp86vTRFVJgpjF9jiIGPEEqYqlDwgyBgEF109VFjmqGmIY/Y4HV4d3Gp2irVfcrp" crossorigin="anonymous">
</svelte:head>

<div class="containers">
  <div id="navigation-bar">
    <nav>
      <ul>
        <li>
          <a href="/" id="logo" use:link>
            <i class="fab fa-autoprefixer fa-2x"></i>
          </a>
        </li>
        <li><a href="/projects" use:link>Projects</a></li>
        <li><a href="/contact" use:link>Contact</a></li>
        <!-- svelte-ignore a11y-invalid-attribute -->
        <!-- svelte-ignore a11y-missing-content -->
        <a href="#" id="menu-icon" />
      </ul>
    </nav>
  </div>
</div>
