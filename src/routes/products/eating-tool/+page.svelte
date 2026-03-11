<script>
  import { base } from '$app/paths';
  import ModelViewer from '$lib/components/ModelViewer.svelte';
</script>

<svelte:head>
  <title>Universal Eating Tool - Level The Curve</title>
</svelte:head>

<section class="product-page">
  <h1 class="section-title">UNIVERSAL EATING TOOL</h1>
  <p class="highlight">Helping individuals with low hand dexterity use eating utensils</p>

  <div class="hero-image">
    <img src="{base}/img/ezadapt.png" alt="Size Medium Universal Eating Tools" />
    <p class="caption">Size Medium Universal Eating Tools</p>
  </div>

  <h2 class="process-title">INTERACTIVE 3D MODEL</h2>
  <p class="viewer-subtitle">Explore the eating tool in 3D — rotate, zoom, and inspect every detail</p>
  <ModelViewer modelUrl="{base}/models/eating-tool.stl" />

  <div class="description">
    <p>
      At Level The Curve, we aim to make everyday life easier for people by creating products that adapt to the customers' needs and wants, and at a low price. The result is a consumer-oriented approach which caters specifically to, as our name suggests, "leveling the curve" as well as the "playing field" for the disabled community.
    </p>
  </div>

  <div class="marquee-wrapper">
    <div class="marquee">
      <span>BUY EATING TOOL NOW &mdash;&mdash; BUY EATING TOOL NOW &mdash;&mdash; BUY EATING TOOL NOW &mdash;&mdash; BUY EATING TOOL NOW &mdash;&mdash; BUY EATING TOOL NOW &mdash;&mdash; BUY EATING TOOL NOW &mdash;&mdash;</span>
      <span>BUY EATING TOOL NOW &mdash;&mdash; BUY EATING TOOL NOW &mdash;&mdash; BUY EATING TOOL NOW &mdash;&mdash; BUY EATING TOOL NOW &mdash;&mdash; BUY EATING TOOL NOW &mdash;&mdash; BUY EATING TOOL NOW &mdash;&mdash;</span>
    </div>
  </div>

  <h2 class="process-title">PROCESS</h2>

  <div class="video-section">
    <iframe
      width="700"
      height="394"
      src="https://www.youtube.com/embed/-7mQb5E_SMI"
      frameborder="0"
      allowfullscreen
      title="Video testimony of Eating Tools being used"
    ></iframe>
    <p class="caption">Video testimony of Eating Tools being used</p>
  </div>

  <div class="process-images">
    <div class="process-image">
      <img src="{base}/img/ezadapt.png" alt="Eating Tool prototype by Apoorva Avadhana" />
      <p class="caption">Eating Tool prototype by Apoorva Avadhana</p>
    </div>
    <div class="process-image">
      <img src="{base}/img/large.png" alt="Modified Eating Tool with Latch by David White Wolf" />
      <p class="caption">Modified Eating Tool with Latch by David White Wolf</p>
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

  .viewer-subtitle {
    font-family: 'Inter', sans-serif;
    font-size: 14px;
    color: #555;
    margin-bottom: 10px;
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

  .marquee-wrapper {
    overflow: hidden;
    background-color: #F5D547;
    padding: 12px 0;
    margin: 40px 0;
  }

  .marquee {
    display: flex;
    width: max-content;
    animation: scroll 20s linear infinite;
  }

  .marquee span {
    font-family: 'Inter', sans-serif;
    font-size: 14px;
    font-weight: 600;
    letter-spacing: 2px;
    white-space: nowrap;
    padding-right: 20px;
  }

  @keyframes scroll {
    0% { transform: translateX(0); }
    100% { transform: translateX(-50%); }
  }

  .video-section {
    margin: 30px auto;
  }

  .video-section iframe {
    max-width: 100%;
    border-radius: 4px;
  }

  .process-images {
    display: flex;
    gap: 30px;
    justify-content: center;
    margin-top: 40px;
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
