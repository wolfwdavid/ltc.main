<svelte:head>
  <title>Gallery - Level The Curve</title>
</svelte:head>

<section class="gallery">
  <h1 class="section-title">GALLERY</h1>
  <p class="subtitle">A look at our journey and our work</p>
  <div class="gallery-grid">
    <!-- Gallery images will go here -->
  </div>
</section>

<style>
  .gallery {
    padding: 60px 40px;
    max-width: 1100px;
    margin: auto;
    text-align: center;
  }

  .subtitle {
    font-family: 'Inter', sans-serif;
    font-size: 14px;
    color: #555;
    margin-bottom: 40px;
  }

  .gallery-grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
  }
</style>
