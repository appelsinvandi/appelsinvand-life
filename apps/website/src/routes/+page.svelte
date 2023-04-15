<script>
  import BobbingParticle from '../components/BobbingParticle/BobbingParticle.svelte'
  import WavesSmall from '../components/WavesSmall/WavesSmall.svelte'
  import WavesBig from '../components/WavesBig/WavesBig.svelte'
  import FallingParticles from '../components/FallingParticles/FallingParticles.svelte'
</script>

<svelte:head>
  <title>🍊🌊</title>
  <meta name="description" content="Det er min appelsinvand" />
</svelte:head>

<div class="appelsinvand">
  <WavesSmall />
  <WavesBig />
  <BobbingParticle particle="🍊" />
</div>

<style lang="scss">
  .appelsinvand {
    position: relative;
    width: 100%;
    height: 100%;
    overflow: hidden;

    display: flex;
    justify-content: center;
    align-items: center;

    background-color: orange;
  }
</style>
