<script>
  import { fade } from "svelte/transition";
  import { linear } from "svelte/easing";

  import Laptop from "../components/Laptop.svelte";
  import LargeCard from "../components/LargeCard.svelte";
  import MainContent from "../components/MainContent.svelte";
  import ProfileCard from "../components/ProfileCard.svelte";

  const options = { duration: 1000, easing: linear };
</script>

<div transition:fade={options}>
  <Laptop />
  <MainContent />
  <div class="me">
    <ProfileCard />
  </div>
  <div class="me">
    <LargeCard />
  </div>
</div>

<style>
  .me {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    max-width: 100%;
  }
</style>
