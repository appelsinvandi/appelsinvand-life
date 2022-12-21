<script lang="ts">
  export let particle: string

  let horizontalOffset = 120 * Math.random() - 10
  let distance = Math.round(10 + 10 * Math.random())
  let falltime = 10 + 10 * Math.random()
  let delay = 20 * Math.random()
  let swaySpeed = 2 + 2 * Math.random()
</script>

<span
  class="particle"
  role="img"
  aria-label="particle"
  style="
    --sway-speed: {swaySpeed}s;
    --horizontal-offset: {horizontalOffset}%;
    --distance: {distance}px;
    --falltime: {falltime}s;
    --delay: {delay}s;
  "
>
  {particle}
</span>

<style lang="scss">
  @keyframes FallingAnimation {
    0% {
      top: -10%;
    }
    100% {
      top: 110%;
    }
  }

  @keyframes SwayingAnimation {
    0% {
      margin-left: 24px;
      margin-right: 0px;
    }
    50% {
      margin-left: 0px;
      margin-right: 24px;
    }
    100% {
      margin-left: 24px;
      margin-right: 0px;
    }
  }

  .particle {
    position: absolute;
    top: -10%;
    left: var(--horizontal-offset);
    z-index: var(--distance);

    font-family: sans-serif;
    color: white;
    font-size: var(--distance);

    animation: var(--falltime) linear var(--delay) infinite FallingAnimation,
      var(--sway-speed) ease-in-out var(--delay) infinite SwayingAnimation;

    user-select: none;
    cursor: default;
  }
</style>
