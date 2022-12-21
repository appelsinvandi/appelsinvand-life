<script>
</script>

<main id="App">
  <slot />
</main>

<style lang="scss">
  #App {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;

    display: flex;
    flex-flow: row nowrap;
    justify-content: center;
    align-items: center;

    overflow: hidden;
  }
</style>
