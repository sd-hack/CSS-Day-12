# CSS-Day-12
<!DOCTYPE html>
<html>
<head>
  <title>Pseudo Classes & Elements</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f2f2f2;
      padding: 30px;
    }

    h2 {
      margin-top: 30px;
    }

    /* ===== Task 1: Services List ===== */

    ul.services {
      list-style: none;
      padding: 0;
      max-width: 300px;
    }

    ul.services li {
      background: white;
      padding: 12px;
      margin-bottom: 8px;
      transition: 0.3s;
    }

    /* Hover effect */
    ul.services li:hover {
      background: #333;
      color: white;
      cursor: pointer;
    }

    /* Alternate styling */
    ul.services li:nth-child(odd) {
      background: #ddd;
    }

    /* Emoji before each item */
    ul.services li::before {
      content: "👉 ";
    }

    /* Reduce opacity except Marketing */
    ul.services li:not(.marketing) {
      opacity: 0.6;
    }

    ul.services li.marketing {
      opacity: 1;
      font-weight: bold;
    }

    /* ===== Task 2: Contact Form ===== */

    .form-box {
      background: white;
      padding: 20px;
      max-width: 300px;
      margin-top: 15px;
      border-radius: 5px;
    }

    .form-box input {
      width: 100%;
      padding: 8px;
      margin-bottom: 12px;
      border: 1px solid #aaa;
      outline: none;
    }

    /* Focus highlight */
    .form-box input:focus {
      border-color: #4caf50;
      background: #e8f5e9;
    }

    .form-box button {
      padding: 10px;
      width: 100%;
      background: #2196f3;
      color: white;
      border: none;
      cursor: pointer;
      position: relative;
      font-size: 16px;
    }

    /* Button hover */
    .form-box button:hover {
      background: #0b7dda;
    }

    /* Arrow after button */
    .form-box button::after {
      content: " ➡️";
    }

  </style>
</head>

<body>

  <h2>Our Services</h2>

  <ul class="services">
    <li>Design</li>
    <li class="marketing">Marketing</li>
    <li>Development</li>
    <li>Support</li>
  </ul>

  <h2>Contact Us</h2>

  <div class="form-box">
    <input type="text" placeholder="Your Name">
    <input type="email" placeholder="Your Email">
    <button>Send</button>
  </div>

</body>
</html>
