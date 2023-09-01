<script lang="ts">
  
</script>

<section>
  <div class={`indexHeader w-full h-screen bg-mainBG text-whitesmoke flex flex-row justify-center items-center text-center`}>
    <div class="clipped p-2 w-[500px] bg-whitesmoke">
      <div class={`textHeader clipped bg-[#ffb6bb] w-[100%] text-center py-4`}>
        <p class="text-5xl animate-pulse">
          Suphakit P.
        </p>
      </div>
    </div>
  </div>
</section>

<style>
  .indexHeader {
    animation: afterLoad .3s;
  }

  .clipped {
    clip-path: polygon(5% 0%, 100% 0%, 100% 80%, 95% 100%, 0% 100%, 0% 20%);
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