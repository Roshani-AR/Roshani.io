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
:root {
    --primary-light-green: rgb(223, 241, 231);
    --primary-med-green: hsl(169, 82%, 27%);
    --primary-red: hsl(0, 66%, 54%);

    --neutral-white: hsl(0, 0%, 100%);
    --neutral-med-grey: hsl(186, 15%, 59%);
    --neutral-dark-grey: hsl(187, 24%, 22%);

    font-family: 'Karla', sans-serif;
    font-size: 14px;
    color: var(--neutral-dark-grey);
}

* {
    box-sizing: border-box;
    margin: 0px;
    padding: 0px;
}

body {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    width: 100vw;
    height: 100%;
    padding: 30px;

    background-color: var(--primary-light-green);
}

div.contact-form {
    width: 100%;
    max-width: 700px;
    padding: 24px;

    border-radius: 16px;
    background-color: var(--neutral-white);
    /* box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3); */
}

h1 {
    font-size: 24px;
    padding-bottom: 24px;
}

h4 {
    font-weight: 400;
}

div.success {
    border-radius: 16px;
    padding: 16px;
    width: fit-content;
    height: 0px;
    margin-bottom: 16px;

    background-color: var(--neutral-dark-grey);
    color: var(--neutral-white);

    position: relative;
    opacity: 0;

    transition-property: opacity, height;
    transition-duration: 0.5s;
}

div.success.submitted {
    height: 100px;
    opacity: 1;
}

div.success div.success-header {
    display: flex;
    align-items: center;
    gap: 8px;
    margin-bottom: 8px;
}

div.success-header h2 {
    font-size: 18px; 
}

div.success-header img {
    width: 18px;
    height: 18px;
}

p.required {
    display: inline;
    color: var(--primary-med-green);
}

div.name {
    display: flex;
    gap: 12px;
    margin-bottom: 16px;
}

div.name div {
    flex-grow: 1;
}

input, textarea {
    margin-top: 12px;
}

div.email {
    margin-bottom: 24px;
}

div.query-type {
    margin-bottom: 24px;
}

div.query-options {
    display: flex;
    gap: 12px;
    margin-top: 12px;
}

div.query-options div {
    flex-grow: 1;
}

div.option {
    border: 1px solid var(--neutral-med-grey);
    border-radius: 8px;

    padding: 8px;
    padding-left: 16px;
    padding-right: 16px;

    display: flex;
    align-items: center;
    gap: 16px;

    position: relative;
}

div.option img.radio-selected {
    position: absolute;
    width: 13px;
    height: 13px;

    display: none;
}

div.option:hover {
    border-color: var(--primary-med-green);
}

div.option:has(input[type="radio"]:checked) {
    background-color: var(--primary-light-green);
}

input[type="radio"]:checked + img.radio-selected {
    display: initial;
}

div.option input {
    margin: 0px;
}

div.option label {
    width: 100%;
}

div.message {
    margin-bottom: 16px;
}

div.message textarea {
    height: 108px;
    resize: none;
}

div.contact-consent {
    display: flex;
    align-items: center;
    gap: 16px;

    position: relative;
}

div.contact-consent input {
    z-index: 1;
}

div.contact-consent input:checked {
    appearance: none;
}

div.contact-consent img.checkbox-selected {
    position: absolute;
    width: 13px;
    height: 13px;

    display: none;
    z-index: 3;
}

#contact-consent:checked + img.checkbox-selected {
    display: initial;
}

div.contact-consent:has(#contact-consent:checked) {
    gap: 29px;
}

div.contact-consent-container p.error-message {
    margin-top: 16px;
}

input[type="text"], 
input[type="email"], 
textarea {
    width: 100%;
    height: 32px;
    padding: 8px;
    padding-left: 16px;
    padding-right: 16px;

    font-family: 'Karla', sans-serif;
    font-size: 14px;
    line-height: 150%;

    border: 1px solid var(--neutral-med-grey);
    border-radius: 8px;
}

input[type="text"]:hover, 
input[type="email"]:hover, 
textarea:hover {
    border-color: var(--primary-med-green);
    cursor: pointer;
}

input[type="text"]:focus-visible, 
input[type="email"]:focus-visible, 
textarea:focus-visible {
    border-color: var(--primary-med-green);
    outline-color: var(--primary-med-green);
}

input[type="button"] {
    width: 100%;
    padding: 8px;
    border: 1px solid gray;
    border-radius: 2px;

    font-family: 'Karla', sans-serif;
    font-size: 14px;
    line-height: 120%;

    margin-top: 24px;
    border-width: 0px;
    border-radius: 8px;

    background-color: var(--primary-med-green);
    color: var(--neutral-white);

    transition-property: box-shadow, transform;
    transition-duration: 0.2s;
}

input[type="button"]:hover {
    /* opacity: 0.7; */
    transform: scale(1.02);
    box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.5);
    cursor: pointer;
}

input[type="checkbox"] {
    margin-top: 0px;
}

p.error-message {
    display: none;
    margin-top: 8px;
    color: var(--primary-red);
}

/* Error Styles */

div.first-name.error input,
div.last-name.error input,
div.email.error input,
div.message.error textarea
{
    border-color: var(--primary-red);
}

div.first-name.error p.error-message,
div.last-name.error p.error-message,
div.email.error p.error-message,
div.query-type.error p.error-message,
div.message.error p.error-message,
div.contact-consent-container.error p.error-message
{
    display: block;
}

/* Media Queries */

@media (max-width: 480px) {
    body {
        height: 100%;
    }

    div.name {
        flex-direction: column;
        margin-bottom: 12px;
    }

    div.query-options {
        flex-direction: column;
    }
}
