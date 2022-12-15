<span class="orange" role="img" aria-label="orange">
  &#x1F34A;
</span>

<style lang="scss">
  @keyframes BobbingAnimation {
    0% {
      transform: scale(1);
    }
    50% {
      transform: scale(0.5);
    }
    100% {
      transform: scale(1);
    }
  }

  .orange {
    position: relative;
    z-index: 20;

    font-size: 160px;
    font-family: sans-serif;

    user-select: none;
    cursor: default;

    animation: 1s ease-in-out BobbingAnimation infinite;
  }
</style>
