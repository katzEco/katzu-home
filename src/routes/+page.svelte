<script lang="ts">
	import IndexPage from "$lib/components/IndexPage.svelte";
  import Loading from "$lib/components/Loading.svelte";
	import PreLoad from "$lib/components/PreLoad.svelte";

  let loading: boolean = true
  let count = 0

  const LoadingCount = setInterval(() => {
    if (count === 2) {
      loading = false
    } else if (count === 4 ) {
      clearInterval(LoadingCount)
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
    <IndexPage />
  {/if}
{/if}