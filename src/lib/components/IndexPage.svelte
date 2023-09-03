<script lang="ts">
  import data from "$lib/modules/mainData"

  const Button = "p-4 bg-skyBlue rounded duration-300 hover:opacity-60 hover:scale-90"
</script>

<section>
  <div class={`indexHeader w-full h-screen bg-mainBG text-whitesmoke flex flex-col justify-center items-center text-center gap-4`}>
    <div class="heading-holder">
      <p class="text-5xl py-2">
        {data.sName}
      </p>
      <p class="text-xl py-2 text-[grey]">
        {data.description}
      </p>
    </div>

    <div class="buttonHolder flex flex-row gap-4 justify-center text-center">
      <a href="/about" class={Button}>
        About
      </a>

      <a href="/certs" class={Button}>
        Certificate
      </a>

      <a href="/commission" class={Button}>
        Commission
      </a>

      <a href="/contacts" class={Button}>
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