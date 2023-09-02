<section class="w-full h-screen fixed top-0 bg-mainBG flex flex-row justify-center items-center">
  <div class="preload bg-whitesmoke h-screen">

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