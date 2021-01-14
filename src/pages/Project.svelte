<script>
  import { fade } from "svelte/transition";
  import { linear } from "svelte/easing";

  import ProjectContainer from "../components/ProjectContainer.svelte";
  import Divider from "../utils/Divider.svelte";

  const options = { duration: 1000, easing: linear };
</script>

<style>
  img {
    max-width: 400px;
    width: 400px;
  }

  .box {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    max-width: 100%;
  }
</style>

<!-- markup (zero or more items) goes here -->
<div class=''>
  <div transition:fade={options} class="box">
    <img src="images/undraw_Browser_stats_re_j7wy.png" alt="projects" />
  </div>
  <Divider />
  <ProjectContainer />
</div>

