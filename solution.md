# Solution Code - Contact Form with Flexbox

<details>
<summary> Step 1 Solution - Create the Form Structure</summary>
    
HTML – `index.html`

```html
<!-- STEP 1: Create the Form Structure -->
<!-- index.html -->

<!-- Location: inside <section class="card">, directly below <h2>Get in Touch</h2> -->

<!-- NEW CODE BELOW -->
<form action="#" method="post">
  <!-- A fieldset groups related inputs under a titled legend -->
  <fieldset>
    <legend>Contact Information</legend>
    <!-- Inputs for Steps 2–3 will be added inside this fieldset -->
  </fieldset>
</form>
<!-- NEW CODE ENDS -->
```

</details>

<details>
<summary>Step 2 Solution – Add Basic Contact Fields</summary>

HTML – `index.html`

```html
<!-- STEP 2: Add Basic Contact Fields -->
<!-- index.html -->

<!-- Location: inside the FIRST <fieldset> created in Step 1 -->

<!-- Name: label comes before input; for/id must match -->
<div class="field-row">
  <label for="name">Name</label>
  <input id="name" type="text" />
</div>

<!-- Email: use type="email" for built-in validation and mobile keyboards -->
<div class="field-row">
  <label for="email">Email</label>
  <input id="email" type="email" />
</div>
```

</details>  
<details>
<summary>Step 3 Solution – Add a Date Picker</summary>

HTML – `index.html`

```html
<!-- STEP 3: Add a Date Picker -->
<!-- index.html -->

<!-- Location: still inside the SAME <fieldset> (“Contact Information”) -->

<!-- Date picker: label 'for' matches input 'id' so the label is clickable -->
<div class="field-row">
  <label for="date">Preferred Contact Date</label>
  <input id="date" type="date" />
</div>
```

</details>   
<details>

<summary> Step 4 Solution – Add a Radio Button Group</summary>

HTML – `index.html`

```html
<!-- STEP 4: Add a Radio Button Group -->
<!-- index.html -->

<!-- Location: AFTER the first <fieldset>, still inside the same <form> -->

<fieldset>
  <legend>Reason for Contact</legend>

  <!-- Flex container for radios; CSS arranges options in a row -->
  <div class="radio-group">
    <!-- All radios share the SAME name="reason" (single choice) -->
    <!-- Each radio gets a UNIQUE id; label 'for' matches that id -->

    <label for="support">
      <input type="radio" name="reason" id="support" />
      Support
    </label>

    <label for="feedback">
      <input type="radio" name="reason" id="feedback" />
      Feedback
    </label>

    <label for="sales">
      <input type="radio" name="reason" id="sales" />
      Sales
    </label>
  </div>
</fieldset>
```
</details>   



<details>

<summary> Step 5 Solution – Add the Submit Button</summary>

HTML – `index.html`

```html
<!-- STEP 5: Add the Submit Button -->
<!-- index.html -->

<!-- Location: BELOW both <fieldset>s, still inside the same <form> -->

<div class="actions">
  <button type="submit" class="btn">Send Message</button>
</div>
```
</details>   



<details>

<summary> Step 6 Solution – Center the Form with Flexbox (Optional)</summary>

CSS – `styles.css`

```css
/* STEP 6: Center the Form with Flexbox */
/* styles.css */

/* Location: add at the BOTTOM of styles.css so these rules override earlier ones */

/* Center the form card horizontally without affecting header/footer containers */
main.container {
  display: flex;            /* Turn the <main> area into a flex container */
  justify-content: center;  /* Center the .card section horizontally */
}

```

</details>   



<details>

<summary> Step 7 Solution – Adjust Spacing and Style the Submit Area (Optional)</summary>

CSS – `styles.css`

```css
/* STEP 7: Adjust Radio Button Spacing & Submit Alignment */
/* styles.css */

/* Location: keep these overrides at the BOTTOM of styles.css (after Step 6) */

/* Increase/decrease space between radio options (flex gap between children) */
.radio-group {
  gap: 1.5rem; /* try 0.5rem for tighter or 2rem for wider spacing */
}

/* Change where the submit button sits within its flex row */
.actions {
  justify-content: center; /* Alternatives: flex-start (left), flex-end (right) */
}

```
</details>   



<details>
<summary>Final Solution</summary>

HTML – `index.html`

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Contact Form with Flexbox</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>

  <header>
    <div class="container">
      <h1>Contact Form with Flexbox</h1>
      <p>Practice semantic forms and Flexbox alignment</p>
    </div>
  </header>

  <main class="container">
    <section class="card">
      <h2>Get in Touch</h2>

      <!-- STEP 1–5: Complete Contact Form -->
      <form action="#" method="post">

        <!-- Contact Information Section -->
        <fieldset>
          <legend>Contact Information</legend>

          <!-- STEP 2: Basic Fields -->
          <div class="field-row">
            <label for="name">Name</label>
            <input id="name" type="text" placeholder="Your full name" />
          </div>

          <div class="field-row">
            <label for="email">Email</label>
            <input id="email" type="email" placeholder="e.g., your@email.com" />
          </div>

          <!-- STEP 3: Date Picker -->
          <div class="field-row">
            <label for="date">Preferred Contact Date</label>
            <input id="date" type="date" />
          </div>
        </fieldset>

        <!-- STEP 4: Radio Button Group -->
        <fieldset>
          <legend>Reason for Contact</legend>

          <div class="radio-group">
            <label for="support">
              <input type="radio" name="reason" id="support" />
              Support
            </label>

            <label for="feedback">
              <input type="radio" name="reason" id="feedback" />
              Feedback
            </label>

            <label for="sales">
              <input type="radio" name="reason" id="sales" />
              Sales
            </label>
          </div>
        </fieldset>

        <!-- STEP 5: Submit Button -->
        <div class="actions">
          <button type="submit" class="btn">Send Message</button>
        </div>

      </form>
    </section>
  </main>

  <footer>
    <div class="container">
      <p class="muted">© 2025 Your Portfolio</p>
    </div>
  </footer>
</body>
</html>

```

CSS – `styles.css`

```css
/* Page layout */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  background-color: #f6f8fb;
  color: #1f2a37;
  line-height: 1.5;
}

h1, h2, legend {
  margin-bottom: 0.5rem;
  font-weight: bold;
}

p {
  margin: 0 0 1rem;
}

header, footer {
  background-color: #ffffff;
  padding: 1rem;
  border-bottom: 1px solid #ddd;
}

footer {
  border-top: 1px solid #ddd;
  text-align: center;
}

.container {
  max-width: 760px;
  margin: 0 auto;
  padding: 1rem;
  text-align: center;
}

/* Card wrapper for form */
.card {
  background-color: #ffffff;
  border: 1px solid #ddd;
  border-radius: 8px;
  padding: 1rem;
}

/* Form layout */
form {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

fieldset {
  border: 1px solid #ddd;
  border-radius: 6px;
  padding: 1rem;
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
}

label {
  font-size: 0.95rem;
}

/* Input rows for label + input alignment */
.field-row {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}

input, textarea, button {
  font: inherit;
}

input, textarea {
  width: 60%;
  border: 1px solid #ccc;
  border-radius: 6px;
  padding: 0.5rem;
}

.textarea {
  min-height: 100px;
}

.radio-group {
  display: flex;
  flex-direction: row;
  gap: 1rem;
}

.actions {
  display: flex;
  justify-content: flex-end;
}

.btn {
  padding: 0.5rem 1rem;
  border: none;
  border-radius: 20px;
  background-color: #2563eb;
  color: #fff;
  cursor: pointer;
}

.btn:hover {
  background-color: #1e4db7;
}

/* Helpers */
.muted {
  color: #6b7280;
}

/* ===== STEP 6: Center the Form with Flexbox ===== */
/* Centers the card horizontally without affecting header/footer */
main.container {
  display: flex;
  justify-content: center;
}

/* ===== STEP 7: Adjust Radio Button Spacing & Submit Alignment ===== */
/* Increases spacing between radio options */
.radio-group {
  gap: 1.5rem;
}

/* Centers the submit button for visual balance */
.actions {
  justify-content: center;
}
```

</details>
