<svelte:head>
  <title>Contact Us - Level The Curve</title>
</svelte:head>

<section class="contact">
  <div class="contact-container">
    <h2 class="section-title">CONTACT US</h2>
    <p class="subtitle">If you wish to contact us, you can do so here.</p>

    <form class="contact-form" action="#" method="post">
      <div class="form-row">
        <div class="form-group">
          <label for="first-name">Name <small>(required)</small></label>
          <input type="text" id="first-name" name="first-name" placeholder="First Name" required />
        </div>
        <div class="form-group">
          <label for="last-name">&nbsp;</label>
          <input type="text" id="last-name" name="last-name" placeholder="Last Name" required />
        </div>
      </div>

      <div class="form-group">
        <label for="email">Email <small>(required)</small></label>
        <input type="email" id="email" name="email" required />
      </div>

      <div class="form-group">
        <label for="subject">Subject <small>(required)</small></label>
        <input type="text" id="subject" name="subject" required />
      </div>

      <div class="form-group">
        <label for="message">Message <small>(required)</small></label>
        <textarea id="message" name="message" rows="5" required></textarea>
      </div>

      <button type="submit" class="submit-btn">SUBMIT</button>
    </form>
  </div>
</section>

<div class="signup-cta">
  <p><strong>IF YOU WOULD LIKE TO HEAR MORE ABOUT US IN THE FUTURE, SIGN UP BELOW!</strong></p>
  <a href="#signup" class="signup-button">SIGN UP</a>
</div>

<style>
  .contact {
    padding: 60px 40px;
    background-color: #fff;
    text-align: center;
  }

  .contact-container {
    max-width: 700px;
    margin: auto;
  }

  .subtitle {
    margin-bottom: 30px;
    font-weight: 300;
    color: #555;
    letter-spacing: 0.5px;
    font-size: 14px;
    font-family: 'Inter', sans-serif;
  }

  .contact-form {
    text-align: left;
  }

  .form-row {
    display: flex;
    gap: 20px;
    flex-wrap: wrap;
  }

  .form-group {
    flex: 1;
    display: flex;
    flex-direction: column;
    margin-bottom: 20px;
  }

  .form-group label {
    margin-bottom: 5px;
    font-size: 13px;
    color: #333;
    font-family: 'Inter', sans-serif;
  }

  .form-group input,
  .form-group textarea {
    padding: 10px;
    font-size: 15px;
    border: 1px solid #ccc;
    border-radius: 2px;
    font-family: 'Inter', sans-serif;
  }

  textarea {
    resize: vertical;
  }

  .submit-btn {
    padding: 12px 30px;
    background-color: #000;
    color: white;
    border: none;
    border-radius: 2px;
    cursor: pointer;
    font-weight: 600;
    letter-spacing: 1.5px;
    font-family: 'Inter', sans-serif;
    font-size: 12px;
    transition: background-color 0.3s ease;
  }

  .submit-btn:hover {
    background-color: #333;
  }

  .signup-cta {
    margin-top: 40px;
    text-align: center;
    padding: 40px;
  }

  .signup-cta p {
    font-family: 'Inter', sans-serif;
    font-weight: 600;
    color: #333;
    font-size: 13px;
    letter-spacing: 1px;
    margin-bottom: 20px;
  }

  .signup-button {
    display: inline-block;
    padding: 14px 32px;
    font-size: 13px;
    border: 2px solid #000;
    border-radius: 50px;
    text-decoration: none;
    color: #000;
    font-weight: 600;
    font-family: 'Inter', sans-serif;
    letter-spacing: 1.5px;
    transition: all 0.3s ease;
  }

  .signup-button:hover {
    background-color: #000;
    color: #fff;
  }
</style>
