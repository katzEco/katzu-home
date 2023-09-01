<script lang="ts">
	import IndexPage from "$lib/components/IndexPage.svelte";
  import Loading from "$lib/components/Loading.svelte";

  let loading: boolean = true
  let count = 0

  const LoadingCount = setInterval(() => {
    if (count >= 2) {
      loading = false
      clearInterval(LoadingCount)
    }

    count += 1
  }, 1000)
</script>

{#if loading}
  <Loading opacityClass="" />
{:else}
  <Loading opacityClass="loadOut opacity-0" />
  <IndexPage />
{/if}