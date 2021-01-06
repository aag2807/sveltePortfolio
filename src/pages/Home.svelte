<script>
  import Hero from "../components/Hero.svelte";
import LargeCard from "../components/LargeCard.svelte";
  import MainContent from "../components/MainContent.svelte";
</script>

<style>
  .me {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    max-width: 100%;
  }
</style>


<Hero />
<MainContent />
<div class="me">
  <LargeCard />
</div>