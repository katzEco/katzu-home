<section class="w-full h-screen fixed top-0 bg-ctp-base flex flex-row justify-center items-center">
  <div class="preload bg-ctp-text h-screen">

  </div>
</section>

<style>
  .preload {
    animation-name: loadingScreen;
    animation-duration: .8s;
    animation-fill-mode: linear;
  }

  @keyframes loadingScreen {
    0% {
      width: 0;
    }

    50% {
      width: 100%;
      opacity: 1;
    }

    75% {
      opacity: 0;
    }

    100% {
      opacity: 0;
    }
  }
</style>