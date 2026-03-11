<script>
  import { base } from '$app/paths';
</script>

<svelte:head>
  <title>About Us - Level The Curve</title>
</svelte:head>

<section class="about">
  <div class="about-content">
    <div class="about-image">
      <img src="{base}/img/stefan_james_khan.jpg" alt="About Level The Curve" />
    </div>
    <div class="about-text">
      <h2>ABOUT US</h2>
      <p>
        At Level The Curve, we aim to make everyday life easier for people by creating products that adapt to the customers' needs and wants, and at a low price.
        The result is a consumer-oriented approach which caters specifically to, as our name suggests, "leveling the curve" as well as the "playing field" for the disabled community.
      </p>
    </div>
  </div>
</section>

<style>
  .about {
    padding: 60px 40px;
    background-color: #f9f9f9;
  }

  .about-content {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    max-width: 1100px;
    margin: auto;
    gap: 40px;
  }

  .about-image img {
    width: 100%;
    max-width: 500px;
    border-radius: 8px;
  }

  .about-text {
    max-width: 500px;
    text-align: left;
  }

  .about-text h2 {
    font-family: 'Playfair Display', serif;
    font-weight: 900;
    font-size: 36px;
    text-transform: uppercase;
    letter-spacing: 2px;
    margin-bottom: 20px;
  }

  .about-text p {
    font-family: 'Inter', sans-serif;
    font-size: 16px;
    line-height: 1.8;
    color: #333;
  }
</style>
