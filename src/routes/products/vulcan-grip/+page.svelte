<script>
  import { base } from '$app/paths';
</script>

<svelte:head>
  <title>Vulcan Grip - Level The Curve</title>
</svelte:head>

<section class="product-page">
  <h1 class="section-title">VULCAN GRIP</h1>
  <p class="highlight">Versatile object holder, clasping onto everyday tools with a 'vulcan' grip</p>

  <div class="hero-image">
    <img src="{base}/img/ezadapt.png" alt="Flexible Strap designed by engineer Apoorva Avadhana" />
    <p class="caption">Flexible Strap designed by engineer Apoorva Avadhana</p>
  </div>

  <div class="description">
    <p>
      At Level The Curve, we aim to make everyday life easier for people by creating products that adapt to the customers' needs and wants, and at a low price. The result is a consumer-oriented approach which caters specifically to, as our name suggests, "leveling the curve" as well as the "playing field" for the disabled community.
    </p>
  </div>

  <h2 class="process-title">PROCESS</h2>

  <div class="process-images">
    <div class="process-image">
      <img src="{base}/img/ezadapt.png" alt="2017 version of Vulcan Grip" />
      <p class="caption">2017 version of Vulcan Grip</p>
    </div>
    <div class="process-image">
      <img src="{base}/img/large.png" alt="Co-Founder Eli Ramos using 2017 Vulcan Grip" />
      <p class="caption">Co-Founder Eli Ramos using 2017 Vulcan Grip</p>
    </div>
  </div>
</section>

<style>
  .product-page {
    padding: 50px 40px;
    max-width: 900px;
    margin: auto;
    text-align: center;
  }

  .hero-image {
    margin: 30px auto;
    max-width: 600px;
  }

  .hero-image img {
    width: 100%;
    border-radius: 4px;
  }

  .description {
    max-width: 800px;
    margin: 30px auto;
    text-align: center;
  }

  .description p {
    font-family: 'Inter', sans-serif;
    font-size: 14px;
    line-height: 1.8;
    color: #333;
  }

  .process-images {
    display: flex;
    gap: 30px;
    justify-content: center;
    margin-top: 30px;
    flex-wrap: wrap;
  }

  .process-image {
    flex: 1;
    max-width: 400px;
  }

  .process-image img {
    width: 100%;
    border-radius: 4px;
  }
</style>
