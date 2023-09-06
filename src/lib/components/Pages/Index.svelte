<script lang="ts">
  import data from "$lib/modules/mainData"

  const Button = "w-[40%] md:w-full p-4 bg-ctp-sapphire text-ctp-base rounded duration-300 shadow-lg shadow-[grey] hover:shadow-sm hover:opacity-60 hover:scale-90"
</script>

<section>
  <div class={`indexHeader w-full h-screen bg-ctp-base text-ctp-text flex flex-col justify-center items-center text-center gap-8`}>
    <div class="heading-holder p-4 rounded bg-ctp-text flex flex-col gap-2 shadow-lg shadow-ctp-text hover:shadow-ctp-sapphire hover:border-ctp-sapphire hover:border-solid border-ctp-text border-2">
      <div class="!justify-end !text-right w-full">
        <img src={data.image} alt="profile" class="w-[100px] h-auto rounded-[100%] ml-auto border-4 border-ctp-sapphire border-solid p-1">
      </div>
      <div class="!text-left">
        <p class="text-4xl py-2 text-pastel-black">
          {data.sName}
        </p>
        <p class="text-xl py-2 text-[grey]">
          {data.description}
        </p>
      </div>
    </div>

    <div class="buttonHolder w-full md:w-[80%] flex flex-row flex-wrap md:flex-nowrap gap-4 justify-center text-center">
      <a href="/about" class={Button} id="about">
        About
      </a>

      <a href="/certs" class={Button} id="certs">
        Certificate
      </a>

      <a href="/commission" class={Button} id="commission">
        Commission
      </a>

      <a href="/contacts" class={Button} id="contacts">
        Contacts
      </a>
    </div>
  </div>
</section>

<style>
  .indexHeader {
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