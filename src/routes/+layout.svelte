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
    font-family: 'Inter', Arial, sans-serif;
    background-color: #fff;
    color: #000;
  }

  :global(img) {
    max-width: 100%;
    height: auto;
    display: block;
  }

  :global(.highlight) {
    background-color: #F5D547;
    padding: 2px 8px;
    display: inline;
    font-family: 'Inter', sans-serif;
    font-style: italic;
    font-size: 14px;
  }

  :global(.section-title) {
    font-family: 'Playfair Display', serif;
    font-weight: 900;
    font-size: 36px;
    text-transform: uppercase;
    letter-spacing: 2px;
    text-align: center;
    margin-bottom: 16px;
  }

  :global(.caption) {
    font-family: 'Inter', sans-serif;
    font-size: 12px;
    color: #555;
    text-align: center;
    margin-top: 8px;
    font-style: italic;
  }

  :global(.process-title) {
    font-family: 'Playfair Display', serif;
    font-weight: 900;
    font-size: 28px;
    text-transform: uppercase;
    letter-spacing: 2px;
    text-align: center;
    margin: 50px 0 30px;
  }
</style>
