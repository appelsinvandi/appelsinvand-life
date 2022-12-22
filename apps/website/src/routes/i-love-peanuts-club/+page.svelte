<script>
  import BobbingParticle from '../../components/BobbingParticle/BobbingParticle.svelte'
  import FallingParticles from '../../components/FallingParticles/FallingParticles.svelte'
</script>

<svelte:head>
  <title>🥜🥜🥜🥜🥜</title>
  <meta name="description" content="The I Love Peanuts Club" />
</svelte:head>

<div class="peanuts">
  <FallingParticles particle="🥜" />
  <BobbingParticle particle="🥜" />
</div>

<style lang="scss">
  .peanuts {
    position: relative;
    width: 100%;
    height: 100%;
    overflow: hidden;

    display: flex;
    justify-content: center;
    align-items: center;

    background-color: lightblue;
  }
</style>
