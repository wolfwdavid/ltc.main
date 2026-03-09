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
    font-size: 3em;
    margin-bottom: 20px;
  }

  .hero-text h2 {
    font-size: 2em;
  }

  iframe {
    max-width: 100%;
  }
</style>
