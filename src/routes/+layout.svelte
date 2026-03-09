<script>
  import Header from '$lib/components/Header.svelte';
  import Footer from '$lib/components/Footer.svelte';

  let { children } = $props();
</script>

<svelte:head>
  <title>Level The Curve</title>
</svelte:head>

<div id="top">
  <Header />
  <main>
    {@render children()}
  </main>
  <Footer />
</div>

<style>
  :global(*) {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  :global(body) {
    font-family: Arial, sans-serif;
  }

  :global(img) {
    max-width: 100%;
    height: auto;
    display: block;
  }
</style>
