<script lang="ts">
  import { page } from "$app/stores";

  const Button = "p-4 hover:opacity-80 bg-cpt-base hover:bg-ctp-overlay0 hover:text-ctp-sapphire"
  const ActiveButton = `${Button} !opacity-80 !bg-ctp-overlay0 !text-ctp-sapphire`
</script>

<section class="w-full flex flex-row fixed top-0 z-10 bg-ctp-base">
  <div class="left w-full flex flex-row justify-start text-left">
    <a href="/" class={Button}>
      Suphakit P.
    </a>
  </div>
  <div class="right w-full flex-row justify-end text-right py-4">
    {#if $page.url.pathname == '/about'}
      <!-- svelte-ignore a11y-invalid-attribute -->
      <a href="#" class={ActiveButton}>
        About
      </a>
    {:else}
      <a href="/about" class={Button}>
        About
      </a>
    {/if}

    {#if $page.url.pathname == '/certs'}
      <!-- svelte-ignore a11y-invalid-attribute -->
      <a href="#" class={ActiveButton}>
        Certificates
      </a>
    {:else}
      <a href="/certs" class={Button}>
        Certificates
      </a>
    {/if}

    {#if $page.url.pathname == '/commission'}
      <!-- svelte-ignore a11y-invalid-attribute -->
      <a href="#" class={ActiveButton}>
        Commission
      </a>
    {:else}
      <a href="/Commission" class={Button}>
        Certificates
      </a>
    {/if}

    {#if $page.url.pathname == '/contact'}
      <!-- svelte-ignore a11y-invalid-attribute -->
      <a href="#" class={ActiveButton}>
        Contact
      </a>
    {:else}
      <a href="/contact" class={Button}>
        Contact
      </a>
    {/if}
  </div>
</section>