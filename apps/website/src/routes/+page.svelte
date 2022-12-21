<script>
  import BouncingParticle from '../components/BobbingParticle/BobbingParticle.svelte'
  import WavesSmall from '../components/WavesSmall/WavesSmall.svelte'
  import WavesBig from '../components/WavesBig/WavesBig.svelte'
  import FallingParticles from '../components/FallingParticles/FallingParticles.svelte'
</script>

<svelte:head>
  <title>🍊🌊</title>
  <meta name="description" content="Det er min appelsinvand" />
</svelte:head>

<FallingParticles particle="❄" />
<WavesSmall />
<WavesBig />
<BouncingParticle particle="🍊" />

<style lang="scss">
</style>
