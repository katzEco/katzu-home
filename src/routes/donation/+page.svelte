<script lang="ts">
  import { browser } from "$app/environment";

	import Donate from "$lib/components/Pages/Donate.svelte";
  import Loading from "$lib/components/Loading.svelte";
	import PreLoad from "$lib/components/PreLoad.svelte";

  let loading: boolean = true
  let count: number

  if (browser) {
    count = Number(window.localStorage.getItem('count')) - 2
  } else {
    count = 0
  }
  
  const LoadingCount = setInterval(() => {
    if (count === 2) {
      loading = false
    } else if (count === 4 ) {
      loading = false
      clearInterval(LoadingCount)
    }

    count += 1
  }, 1000)
</script>

<svelte:head>
  <title>Donate | Suphakit P.</title>
</svelte:head>

{#if loading}
  <Loading opacityClass="" />
{:else}
  {#if count === 3}
    <Loading opacityClass="loadOut opacity-0" />
    <PreLoad/>
  {:else}
    <Donate />
  {/if}
{/if}