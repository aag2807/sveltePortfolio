<script>
  import { Tabs, Tab, TabContent } from 'svelte-materialify/src';

  import infos from '../shared/about'
</script>

<style>
  .box {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
</style>

<!-- <div class="box"> -->
  <Tabs vertical centered class="mt-2">
    <div slot="tabs">
      {#each infos as info, i}
        <Tab>{info.title}</Tab>
      {/each}
    </div>
  
    <div class="pa-2">
      {#each infos as info, i}
        <TabContent>
          <div class="text-caption text-decoration-underline">{info.overlay}</div>
          <p>
            {@html info.content}
          </p>
        </TabContent>
      {/each}
    </div>
  </Tabs>
  
<!-- </div> -->
