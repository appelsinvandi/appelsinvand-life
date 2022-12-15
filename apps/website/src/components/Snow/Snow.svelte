<script>
  import Snowflake from './Snowflake.svelte'

  let snowflakes =
    typeof window !== 'undefined'
      ? Array.from({ length: window.screen.width }, (_, i) => i)
      : []
</script>

<div class="snow">
  {#each snowflakes as snowflake}
    <Snowflake />
  {/each}
</div>

<style lang="scss">
  .snow {
    position: absolute;
    z-index: 1;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }
</style>
