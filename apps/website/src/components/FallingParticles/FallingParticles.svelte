<script lang="ts">
  import Particle from './_Particle.svelte'

  export let particle: string

  let particles =
    typeof window !== 'undefined'
      ? Array.from({ length: window.screen.width }, (_, i) => i)
      : []
</script>

<div class="falling-particles">
  {#each particles as _}
    <Particle {particle} />
  {/each}
</div>

<style lang="scss">
  .falling-particles {
    position: absolute;
    z-index: 1;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    overflow: hidden;
  }
</style>
