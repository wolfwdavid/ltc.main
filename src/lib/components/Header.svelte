<script>
  import { base } from '$app/paths';
</script>

<header>
  <div class="header-top">
    <div class="logo">
      <a href="{base}/">
        <img src="{base}/img/ltc.png" alt="Level The Curve Logo" />
      </a>
    </div>
    <nav>
      <a href="{base}/">LEVEL THE CURVE</a>
      <a href="{base}/about">ABOUT US</a>
      <a href="{base}/products">PRODUCTS</a>
      <a href="{base}/gallery">GALLERY</a>
      <a href="{base}/contact">CONTACT US</a>
      <a href="{base}/consultations">CONSULTATIONS</a>
      <a href="{base}/donations">DONATIONS</a>
    </nav>
  </div>
  <div class="tagline">Access. Independence. Dignity.</div>
</header>

<style>
  header {
    padding: 20px 40px 10px;
    background-color: #fff;
  }

  .header-top {
    display: flex;
    align-items: center;
    gap: 40px;
  }

  .logo img {
    height: 45px;
  }

  .logo a {
    text-decoration: none;
  }

  nav {
    display: flex;
    gap: 28px;
    flex-wrap: wrap;
  }

  nav a {
    text-decoration: none;
    color: #000;
    font-family: 'Inter', sans-serif;
    font-size: 12px;
    font-weight: 500;
    letter-spacing: 1.5px;
    text-transform: uppercase;
  }

  nav a:hover {
    text-decoration: underline;
  }

  .tagline {
    font-family: 'Inter', sans-serif;
    font-size: 13px;
    color: #333;
    margin-top: 8px;
    font-style: italic;
    letter-spacing: 0.5px;
  }
</style>
