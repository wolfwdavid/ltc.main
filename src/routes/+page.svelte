<section class="hero">
  <video autoplay muted loop id="background-video">
    <source src="/path-to-video.mp4" type="video/mp4" />
    Your browser does not support the video tag.
  </video>
  <div class="hero-text">
    <iframe
      width="560"
      height="315"
      src="https://www.youtube.com/embed/-7mQb5E_SMI"
      frameborder="0"
      allowfullscreen
      title="Level The Curve - Our Story"
    ></iframe>
    <h1>THIS IS WHY WE DO WHAT WE DO</h1>
    <h2>Level The Curve - Our Story</h2>
  </div>
</section>

<style>
  .hero {
    position: relative;
    height: 100vh;
    overflow: hidden;
    background-color: #000;
  }

  #background-video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .hero-text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    color: white;
  }

  .hero-text h1 {
    font-family: 'Playfair Display', serif;
    font-size: 3em;
    font-weight: 900;
    margin-bottom: 20px;
    letter-spacing: 2px;
  }

  .hero-text h2 {
    font-family: 'Inter', sans-serif;
    font-size: 1.5em;
    font-weight: 300;
  }

  iframe {
    max-width: 100%;
    margin-bottom: 20px;
  }
</style>
