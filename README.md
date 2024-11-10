<img src="assets/images/icon-s<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- displays site properly based on user's device -->

  <link rel="icon" type="image/png" sizes="32x32" href="./assets/images/favicon-32x32.png">
  
  <title>Frontend Mentor | Contact form</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Karla:ital,wght@0,200..800;1,200..800&display=swap" rel="stylesheet">
  <style>
    .attribution { font-size: 14px; text-align: center; margin-top: 16px; }
    .attribution a { color: hsl(228, 45%, 44%); }
  </style>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <div class="success">
    <div class="success-header">
        uccess-check.svg" alt="Success check">
      <h2>Message Sent!</h2>
    </div>
    <p>Thanks for completing the form. We'll be in touch soon!</p>
  </div>

  <div class="contact-form" id="contact-form">
    <h1>Contact Form</h1>

    <form action="" id="main-form">
      <!-- First name, last name, email -->
      <div class="name">
        <div class="first-name">
          <label for="first-name">First Name <p class="required">*</p></label>
          <input type="text" name="first-name" id="first-name" aria-required="true">
          <p class="error-message">This field is required</p>
        </div>
        <div class="last-name" >
          <label for="last-name">Last Name <p class="required">*</p></label>
          <input type="text" name="last-name" id="last-name" aria-required="true">
          <p class="error-message">This field is required</p>
        </div>
      </div>

      <div class="email">
        <label for="email">Email Address <p class="required">*</p></label>
        <input type="text" name="email" id="email" aria-required="true">
        <!-- Please enter a valid email address -->
        <p class="error-message">Please enter a valid email address</p>
      </div>

      <!-- General enquiry OR support request? -->
      <div class="query-type">
        <h4 class="label">Query Type <p class="required">*</p></h4>
        <div class="query-options">
          <div class="option">
            <input type="radio" name="query-type" id="enquiry" value="enquiry" aria-required="true">
            <img src="assets/images/icon-radio-selected.svg" alt="Radio button selected" class="radio-selected">
            <label for="enquiry">General Enquiry</label>
          </div>
          <div class="option">
            <input type="radio" name="query-type" id="support" value="support">
            <img src="assets/images/icon-radio-selected.svg" alt="Radio button selected" class="radio-selected">
            <label for="support">Support Request</label>
          </div>
        </div>
        <p class="error-message">Please select a query type</p>
      </div>

      <!-- Message -->
      <div class="message">
        <label for="message">Message <p class="required">*</p></label>
        <textarea name="message" id="message" aria-required="true"></textarea>
        <p class="error-message">This field is required</p>
      </div>

      <!-- Consent to contact -->
      <div class="contact-consent-container">
        <div class="contact-consent">
          <input type="checkbox" name="contact-consent" id="contact-consent" aria-required="true">
          <img src="assets/images/icon-checkbox-check.svg" alt="Icon radio selected" class="checkbox-selected">
          <label for="contact-consent" class="contact-consent-label">I consent to being contacted by the team. <p class="required">*</p></label>
        </div>
        <p class="error-message">To consent to this form, please consent to being contacted</p>
      </div>
      
      <input type="button" value="Submit" id="submit-form">
    </form>
  </div>

  <div class="attribution">
  </div>

  <script src="script.js"></script>
</body>
</html>

    }

    div.query-options {
        flex-direction: column;
    }
}
