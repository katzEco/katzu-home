<script lang="ts">
  import Navbar from "$lib/components/Navbar.svelte";
	import Footer from "$lib/components/Footer.svelte"
  import UserData from "$lib/modules/mainData";

  const data = UserData.donate
</script>

<section>
  <Navbar />
  <div class="contentContainer w-full md:w-[90%] mx-auto">
    <div class="w-full py-6"></div>
    <div class="header w-full h-[40vh] mx-auto !bg-center !bg-cover !bg-no-repeat md:rounded-b relative z-0" style="background: url(https://frame.caffe.quest/cdn);">
      <div class="w-full h-full bg-[rgba(0,0,0,0.7)] flex flex-col items-center justify-center text-center backdrop-blur-md md:rounded-b z-10">
        <p class="text-4xl py-4 text-ctp-text">
          Donate
        </p>
        <p class="text-ctp-text opacity-50">
          Aha! I know you will find this page one day :D
        </p>
      </div>
    </div>

    <div class="info relative mt-[-2rem] mx-auto p-6 w-[80%] bg-ctp-text text-ctp-base rounded-t z-20">
      <div class="w-full mx-auto text-lg">
        <div class="w-[80%] mx-auto gap-4 gap-y-6 flex flex-row flex-wrap text-center justify-center">
          {#each data as event }
            <div class="bg-ctp-base p-4 rounded w-[80%] text-center">
              <p class="text-xl text-ctp-text py-2">
                {event.Address}
              </p>
              <p class="text-[15px] text-ctp-subtext1 py-2">
                {event.Receiver}
              </p>
            </div>
          {/each}
        </div>
      </div>
    </div>
  </div>
  <Footer />
</section>

<style>
  .contentContainer {
    animation: afterLoad .3s;
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