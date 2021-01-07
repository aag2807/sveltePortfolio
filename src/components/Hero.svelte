<script>
  import HomeCard from "./HomeCard.svelte";
</script>

<style>
  img {
    max-width: 100%;
    max-height: 100%;
  }

  .sub {
    color: #e65100;
  }

  .box {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }

  .box-s {
    margin: 0;
    padding: 0;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  @media screen and (max-width: 600px) {
    .temp {
      display: none;
    }
  }
</style>

<!-- markup (zero or more items) goes here -->
<div class="box">
  <h3 class="text-h3 text-center">Hi, I'm Alvaro</h3>
  <h4 class="text-h4 sub text-center">Full-Stack Developer</h4>
  <div class="text-caption text-center">In Dominican Republic.</div>
</div>

<div class="box-s">
  <div class="temp">
    <HomeCard 
      overline="Full-Stack" 
      headline="Front-End" 
      content='Javascript<br>Nerd'
      url={'/projects'}
    />
  </div>
  <!-- image -->
  <img
    src="images/drawkit-full-stack-man-monochrome-400px.png"
    width="450px"
    alt="" />
  <!-- / image -->
  <div class="temp">
    <HomeCard 
      overline="Full-Stack" 
      headline="Back- End"
      content='Programmer<br>language Fan'
      url={'/projects'}
      />
  </div>
</div>
