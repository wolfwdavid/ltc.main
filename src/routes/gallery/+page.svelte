<svelte:head>
  <title>Gallery - Level The Curve</title>
</svelte:head>

<section class="gallery">
  <div class="gallery-content">
    <h2>Gallery</h2>
    <div class="gallery-grid">
      <!-- Gallery images will go here -->
    </div>
  </div>
</section>

<style>
  .gallery {
    padding: 60px 20px;
    background-color: #f9f9f9;
  }

  .gallery-content {
    max-width: 1200px;
    margin: auto;
    text-align: center;
  }

  .gallery-content h2 {
    font-size: 32px;
    margin-bottom: 30px;
  }

  .gallery-grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
  }
</style>
