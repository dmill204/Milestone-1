<section id="Home">
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, inittial-scale=1.0">
</head>
  <button id="themeToggle">Dark Mode</button>

  <script>
    const body = document.body;
    const themeToggle = document.getElementById('themeToggle');

    themeToggle.addEventListener('click', () => {
      body.classList.toggle('dark-mode');
    });
  </script>
<body>
    <header>
        <h1>Welcome to My Website - Daniel Miller</h1>
        <nav>
            <ul>
                <li><a href="https://dmill204.github.io/Web_Page/">Home</a></li>
                <li><a href="https://dmill204.github.io/About_Page/">About</a></li>
                <li><a href="https://dmill204.github.io/Contact_Page/">Contact</a></li>
            </ul>
        </nav>
    </header>
    <main>
    </main>
    <footer>
    </footer>
</body>
</html>
</section>
