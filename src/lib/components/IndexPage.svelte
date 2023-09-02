<script lang="ts">
  const Button = "clipped-button p-2 bg-whitesmoke duration-300 hover:opacity-60"

  const InnerButton = "w-full clipped-button p-4 bg-skyBlue"
</script>

<section>
  <div class={`indexHeader w-full h-screen bg-mainBG text-whitesmoke flex flex-col justify-center items-center text-center gap-6`}>
    <div class="clipped p-2 w-[600px] bg-whitesmoke">
      <div class={`textHeader clipped bg-[#fe6e6f] w-[100%] text-center py-4`}>
        <p class="text-5xl text-whitesmoke">
          Suphakit P.
        </p>
      </div>
    </div>

    <div class="flex flex-row flex-wrap justify-center gap-4">
      <a class={Button} href="#About">
        <div class="w-full clipped-button p-4 bg-skyBlue">
          About Me
        </div>
      </a>

      <a class={Button} href="/certificate">
        <div class={InnerButton}>
          Certificates
        </div>
      </a>

      <a class={Button} href="/commission">
        <div class={InnerButton}>
          Commission
        </div>
      </a>
      
      <a class={Button} href="/contact">
        <div class={InnerButton}>
          Contact
        </div>
      </a>
    </div>
  </div>
</section>

<style>
  .indexHeader {
    animation: afterLoad .3s;
  }

  .clipped {
    border-top-left-radius: 1rem;
    border-bottom-right-radius: 1rem;
  }

  .clipped-button {
    border-top-left-radius: 1rem;
    border-bottom-right-radius: 1rem;
  }

  @keyframes afterLoad {
    from {
      opacity: 0;
    }

    to {
      opacity: 1;
    }
  }
</style>