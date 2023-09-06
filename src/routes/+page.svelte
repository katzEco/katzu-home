<script lang="ts">
  import { browser } from "$app/environment";

	import Index from "$lib/components/Pages/Index.svelte";
  import Loading from "$lib/components/Loading.svelte";
	import PreLoad from "$lib/components/PreLoad.svelte";

  let loading: boolean = true
  let count = 0

  const LoadingCount = setInterval(() => {
    if (count === 2) {
      loading = false
    } else if (count === 4 ) {
      clearInterval(LoadingCount)
      if (browser) {
        window.localStorage.setItem('count', String(count))
      }
    }

    count += 1
  }, 1000)
</script>

<svelte:head>
  <title>Index | Suphakit P.</title>
</svelte:head>

{#if loading}
  <Loading opacityClass="" />
{:else}
  {#if count == 3}
    <Loading opacityClass="loadOut opacity-0" />
    <PreLoad/>
  {:else}
    <Index />
  {/if}
{/if}