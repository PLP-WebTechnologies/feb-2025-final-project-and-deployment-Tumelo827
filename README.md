# Final Project and Deployment

## Objectives
Build a fully functional web application.
Apply HTML, CSS, and JavaScript concepts learned.
Deploy the project using GitHub Pages, Netlify, or Vercel.

## Instructions
Choose one of the following project ideas:
Blog Website: Implement a multi-page site with navigation.
Ecommerce Website: Implement a multi-page site with navigation.

>[!NOTE]
> - Include at least:
> - A responsive design.
> - JavaScript interactivity.
> - A deployment link.

## Tasks

Create a well-structured HTML5 document.
Use at least 5 different HTML elements.
Ensure semantic correctness.

Good luck and happy coding! 🚀💻



<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>My Blog</title>
  <style>
    /* General styles */
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background: #fafafa;
      color: #333;
    }

    header {
      background-color: #0077cc;
      color: white;
      padding: 20px;
      text-align: center;
    }

    nav ul {
      list-style: none;
      display: flex;
      justify-content: center;
      padding: 0;
      flex-wrap: wrap;
    }

    nav ul li {
      margin: 10px 15px;
    }

    nav ul li a {
      color: white;
      text-decoration: none;
      font-weight: bold;
    }

    main {
      padding: 20px;
    }

    .post {
      background: #fff;
      margin-bottom: 20px;
      padding: 15px;
      border-left: 5px solid #0077cc;
      cursor: pointer;
      transition: background 0.3s;
    }

    .post:hover {
      background: #f0f8ff;
    }

    form {
      max-width: 600px;
      margin: 40px auto;
      background: #fff;
      padding: 20px;
      border: 1px solid #ddd;
      border-radius: 6px;
    }

    form input,
    form textarea {
      width: 100%;
      margin-bottom: 15px;
      padding: 10px;
      font-size: 16px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }

    form button {
      background-color: #0077cc;
      color: white;
      padding: 10px 20px;
      border: none;
      cursor: pointer;
      border-radius: 4px;
    }

    footer {
      text-align: center;
      padding: 15px;
      background: #eee;
      margin-top: 40px;
    }

    /* Responsive design */
    @media (max-width: 768px) {
      nav ul {
        flex-direction: column;
        align-items: center;
      }

      .post {
        font-size: 90%;
      }

      form {
        margin: 20px;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>Welcome to My Blog</h1>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <!-- Home Section -->
    <section id="home">
      <h2>Latest Posts</h2>

      <div class="post" onclick="alert('You clicked the post!')">
        <h3>How to Build Your First Website</h3>
        <p>Learn the steps to create and deploy a simple website using HTML, CSS, and JavaScript.</p>
      </div>

      <div class="post">
        <h3>Why Responsive Design Matters</h3>
        <p>Discover how responsive layouts make your website mobile-friendly and future-proof.</p>
      </div>
    </section>

    <!-- About Section -->
    <section id="about">
      <h2>About Me</h2>
      <p>Hello! I'm a passionate web developer sharing tips and tutorials through my blog. Thanks for visiting!</p>
    </section>

    <!-- Contact Section -->
    <section id="contact">
      <h2>Contact Me</h2>
      <form onsubmit="return validateForm()">
        <label for="name">Name:</label>
        <input type="text" id="name" required placeholder="Your Name" />

        <label for="email">Email:</label>
        <input type="email" id="email" required placeholder="you@example.com" />

        <label for="message">Message:</label>
        <textarea id="message" required placeholder="Write your message here..."></textarea>

        <button type="submit">Send</button>
      </form>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 My Blog</p>
  </footer>

  <script>
    function validateForm() {
      const name = document.getElementById("name").value.trim();
      const email = document.getElementById("email").value.trim();
      const message = document.getElementById("message").value.trim();

      if (!name || !email || !message) {
        alert("Please fill out all fields.");
        return false;
      }

      alert("Thank you, " + name + "! Your message has been sent.");
      return true;
    }
  </script>
</body>
</html>
