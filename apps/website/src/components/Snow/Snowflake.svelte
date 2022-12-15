<script lang="ts">
  let horizontalOffset = 120 * Math.random() - 10
  let distance = Math.round(10 + 10 * Math.random())
  let falltime = 10 + 10 * Math.random()
  let delay = 20 * Math.random()
  let swaySpeed = 2 + 2 * Math.random()
  let rotationSpeed = 4 + 4 * Math.random()
</script>

<span
  class="snowflake"
  role="img"
  aria-label="snowflake"
  style="
    --sway-speed: {swaySpeed}s;
    --rotation-speed: {rotationSpeed}s;
    --horizontal-offset: {horizontalOffset}%;
    --distance: {distance}px;
    --falltime: {falltime}s;
    --delay: {delay}s;
  "
>
  &#x2744;
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

  @keyframes RotatingAnimation {
    0% {
      transform: rotate(-24deg);
    }
    50% {
      transform: rotate(24deg);
    }
    100% {
      transform: rotate(-24deg);
    }
  }

  .snowflake {
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
