<script lang="ts">
  import Navbar from "$lib/components/Navbar.svelte";
	import Footer from "$lib/components/Footer.svelte"
  import TW_CLASS from "$lib/constants/tailwind";
  import UserData from "$lib/modules/mainData";

  const data = UserData.commission
</script>

<section>
  <Navbar />
  <div class="contentContainer w-full md:w-[90%] mx-auto">
    <div class="w-full py-6"></div>
    <div class="header w-full h-[40vh] mx-auto !bg-center !bg-cover !bg-no-repeat md:rounded-b relative z-0" style="background: url(https://frame.caffe.quest/cdn);">
      <div class="w-full h-full bg-[rgba(0,0,0,0.7)] flex flex-col items-center justify-center text-center backdrop-blur-md md:rounded-b z-10">
        <p class="text-4xl py-4 text-ctp-text">
          Commission
        </p>
        <p class="text-ctp-text opacity-50">
          Love my works? Just hire me :)
        </p>
      </div>
    </div>

    <div class="info relative mt-[-2rem] mx-auto p-6 w-[80%] bg-ctp-text text-ctp-base rounded-t z-20">
      <div class="w-full mx-auto text-lg">
        <p class="py-4 underline text-2xl w-[80%] mx-auto">
          Music Works
        </p>

        <div class="w-[80%] mx-auto gap-2 flex flex-row flex-wrap text-center justify-center">
          {#each data.music as event }
            <div class="w-[18rem] bg-ctp-base text-ctp-text rounded p-1 flex flex-col">
              <div class="p-4">
                <p class={`text-xl`}>
                  {event.name}
                </p>
                <div class="w-[80%] border-solid border-ctp-text border-b-2 mx-auto my-2"></div>
                <p class="text-[15px] text-ctp-subtext1 py-2">
                  {event.desp}
                </p>
                <div class="w-[80%] border-solid border-ctp-text border-b-2 mx-auto my-2"></div>
                <p class="text-[18px] text-ctp-text">
                  {event.price}
                </p>
                <div class="w-[80%] border-solid border-ctp-text border-b-2 mx-auto my-2"></div>
                <div class="text-right py-2 text-[15px]">
                  <a href={data.contact} class={`${TW_CLASS.link} bg-ctp-sapphire !no-underline !text-ctp-base p-2 rounded`}>
                    Contact Me >
                  </a>
                </div>
              </div>
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