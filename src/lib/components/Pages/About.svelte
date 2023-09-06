<script lang="ts">
  import Navbar from "$lib/components/Navbar.svelte";
	import Footer from "$lib/components/Footer.svelte"
  import UserData from "$lib/modules/mainData";

  const data = UserData.about

  const age = new Date().getFullYear() - new Date(Number(data.age)).getFullYear()
</script>

<section>
  <Navbar />
  <div class="contentContainer w-full md:w-[90%] mx-auto">
    <div class="w-full py-6"></div>
    <div class="header w-full h-[40vh] mx-auto !bg-center !bg-cover !bg-no-repeat md:rounded-b relative z-0" style="background: url(https://frame.caffe.quest/cdn);">
      <div class="w-full h-full bg-[rgba(0,0,0,0.7)] flex flex-col items-center justify-center text-center backdrop-blur-md md:rounded-b z-10">
        <p class="text-4xl py-4 text-ctp-text">
          About
        </p>
        <p class="text-ctp-text opacity-50">
          Just some information about me~
        </p>
      </div>
    </div>

    <div class="info relative mt-[-2rem] mx-auto p-6 w-[80%] bg-ctp-text text-ctp-base rounded-t z-20">
      <p class="py-4 underline text-2xl w-[80%] mx-auto">
        <strong>
          Information
        </strong>
      </p>
      <div class="w-full mx-auto pb-4 text-lg">
        <p class="py-1 w-[80%] mx-auto">
          <strong>Name</strong>: {data.name}
        </p>
        <p class="py-1 w-[80%] mx-auto">
          <strong>Age</strong>: {age}
        </p>

        <div class="w-[80%] border-solid border-ctp-base border-b-2 mx-auto my-6"></div>

        <p class="py-1 pb-4 underline text-2xl w-[80%] mx-auto">
          <strong>
            Education Profile
          </strong>
        </p>

        <div class="w-full mx-auto gap-4 flex flex-row flex-wrap text-center justify-center pb-8">
          {#each data.education as education}
            <div class="p-4 w-[40%] bg-ctp-base text-ctp-text rounded">
              <p class="text-[18px]">
                {education.school}
              </p>
              <p class="text-[15px] opacity-60">
                {(education.classroom != '') ? education.classroom : '-'}
              </p>
              <p class="text-[15px]">
                {education.grade}
              </p>
              <div class="w-[80%] border-solid border-ctp-text border-b-2 mx-auto my-2"></div>
              <p class="text-[15px]">
                {education.startDate} - {education.endDate}
              </p>
            </div>
          {/each}
        </div>

        <div class="w-[80%] border-solid border-ctp-base border-b-2 mx-auto my-6"></div>

        <p class="py-1 pb-4 underline text-2xl w-[80%] mx-auto">
          <strong>
            Skills
          </strong>
        </p>

        <div class="w-[80%] mx-auto gap-2 flex flex-row flex-wrap text-center justify-center">
          {#each data.skills as skill }
            <a href={skill.link} class={`bg-ctp-base hover:bg-ctp-overlay1 rounded p-2 flex flex-row items-center`} target="_blank">
              <img src={skill.img} alt={skill.alt} class="w-[45px] h-[45px]">
            </a>
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