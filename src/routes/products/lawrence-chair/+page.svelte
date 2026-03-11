<script>
  import { base } from '$app/paths';
</script>

<svelte:head>
  <title>Lawrence Chair - Level The Curve</title>
</svelte:head>

<section class="product-page">
  <h1 class="section-title">LAWRENCE (SPINAL MOBILITY) CHAIR</h1>
  <p class="highlight">Great way to exercise your spine</p>

  <div class="hero-image">
    <img src="{base}/img/large.png" alt="2025 model of Lawrence Chair" />
    <p class="caption">2025 model of Lawrence Chair by David White Wolf and Alisa Mizukami</p>
  </div>

  <div class="description">
    <p>
      At Level The Curve, we aim to make everyday life easier for people by creating products that adapt to the customers' needs and wants, and at a low price. The result is a consumer-oriented approach which caters specifically to, as our name suggests, "leveling the curve" as well as the "playing field" for the disabled community.
    </p>
  </div>

  <h2 class="process-title">PROCESS</h2>

  <div class="process-images">
    <div class="process-image">
      <img src="{base}/img/large.png" alt="2017 model of Lawrence Chair by Stefan Henry" />
      <p class="caption">2017 model of Lawrence Chair by Stefan Henry</p>
    </div>
    <div class="process-image">
      <img src="{base}/img/large.png" alt="LTC Members taking picture with chair" />
      <p class="caption">LTC Members taking picture with chair</p>
    </div>
  </div>

  <div class="process-single">
    <img src="{base}/img/large.png" alt="Physical prototype of Lawrence Chair" />
    <p class="caption">Physical prototype of Lawrence Chair</p>
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

  .process-single {
    margin: 40px auto;
    max-width: 500px;
  }

  .process-single img {
    width: 100%;
    border-radius: 4px;
  }
</style>
