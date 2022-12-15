<div class="waves-small" />

<style lang="scss">
  @keyframes LevelAnimation {
    0% {
      top: 55%;
    }
    50% {
      top: 45%;
    }
    100% {
      top: 55%;
    }
  }

  @keyframes ScrollAnimation {
    0% {
      background-position-x: 128px;
    }
    100% {
      background-position-x: 0;
    }
  }

  .waves-small {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    z-index: 5;

    background-image: url('data:image/svg+xml,%3Csvg xmlns="http://www.w3.org/2000/svg" xml:space="preserve" width="1024" height="1024"%3E%3Cpath fill="%2300A7BE" d="M0 257.509C256 257.509 256 0 512 0s256 257.509 512 257.509V1024H0V257.509z"/%3E%3C/svg%3E%0A');
    background-position-y: top;
    background-repeat: repeat-x;
    background-size: 128px;

    animation: LevelAnimation 3s ease-in-out infinite,
      ScrollAnimation 2s linear infinite;
    transform: translateY(32px);

    &:after {
      content: '';

      position: absolute;
      top: 64px;
      right: 0;
      bottom: 0;
      left: 0;

      background-color: #00a7be;
    }
  }
</style>
