<svelte:head>
  <title>Contact Us - Level The Curve</title>
</svelte:head>

<section class="contact">
  <div class="contact-container">
    <h2>CONTACT US</h2>
    <p>If you wish to contact us, you can do so here.</p>

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
    padding: 60px 20px;
    background-color: #fff;
    text-align: center;
  }

  .contact-container {
    max-width: 800px;
    margin: auto;
  }

  .contact h2 {
    font-size: 28px;
    margin-bottom: 10px;
  }

  .contact p {
    margin-bottom: 30px;
    font-weight: 300;
    color: #444;
    letter-spacing: 0.5px;
    font-size: 14px;
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
    font-size: 14px;
    color: #333;
  }

  .form-group input,
  .form-group textarea {
    padding: 10px;
    font-size: 16px;
    border: 1px solid #ccc;
    border-radius: 2px;
  }

  textarea {
    resize: vertical;
  }

  .submit-btn {
    padding: 12px 30px;
    background-color: #222;
    color: white;
    border: none;
    border-radius: 2px;
    cursor: pointer;
    font-weight: bold;
    letter-spacing: 1px;
  }

  .submit-btn:hover {
    background-color: #000;
  }

  .signup-cta {
    margin-top: 40px;
    text-align: center;
    padding: 40px 20px;
  }

  .signup-cta p {
    font-weight: bold;
    color: #444;
    font-size: 14px;
    letter-spacing: 1px;
    margin-bottom: 20px;
  }

  .signup-button {
    display: inline-block;
    padding: 14px 32px;
    font-size: 16px;
    border: 2px solid #000;
    border-radius: 50px;
    text-decoration: none;
    color: #000;
    font-weight: bold;
    transition: all 0.3s ease;
  }

  .signup-button:hover {
    background-color: #000;
    color: #fff;
  }
</style>
