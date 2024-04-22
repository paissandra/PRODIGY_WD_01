# PRODIGY_WD_01
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Interactive Navigation Menu</title>
<style>
  body {
    margin: 0;
    font-family: Arial, sans-serif;
    scroll-behavior: smooth;
  }
  nav {
    position: fixed;
    top: 0;
    width: 100%;
    background-color: #e8eaf6; /* Updated menu background color */
    z-index: 1000;
    transition: background-color 0.3s ease;
  }
  nav ul {
    margin: 0;
    padding: 0;
    list-style-type: none;
    display: flex;
    justify-content: center;
  }
  nav li {
    margin: 0 15px;
  }
  nav a {
    color: #3949ab; /* Updated menu link color */
    text-decoration: none;
    padding: 10px 15px;
    display: inline-block;
    transition: color 0.3s ease;
  }
  nav a:hover {
    color: #ff9800; /* Updated hover color */
  }
  /* Updated section colors */
  #home, #about, #services, #contact {
    height: 100vh; /* Full viewport height */
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
  }
  #home {
    background-color: #ffebee; /* Light red */
  }
  #about {
    background-color: #e8f5e9; /* Light green */
  }
  #services {
    background-color: #e3f2fd; /* Light blue */
  }
  #contact {
    background-color: #fff9c4; /* Light yellow */
  }
  /* Center headings horizontally */
  h2 {
    margin: 0;
    text-align: center;
    color: #3949ab; /* Updated heading color */
  }
</style>
</head>
<body>
<nav id="main-menu">
  <ul>
    <li><a href="#home">Home</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<div id="home">
  <h2>Welcome to the Home Section</h2>
</div>
<div id="about">
  <h2>About Us</h2>
</div>
<div id="services">
  <h2>Our Services</h2>
</div>
<div id="contact">
  <h2>Contact Us</h2>
</div>

<script>
  window.addEventListener('scroll', function() {
    var nav = document.getElementById('main-menu');
    if (window.scrollY > 50) {
      nav.style.backgroundColor = '#c5cae9'; /* Updated scroll color */
    } else {
      nav.style.backgroundColor = '#e8eaf6';
    }
  });

  // Smooth scrolling
  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function(e) {
      e.preventDefault();

      document.querySelector(this.getAttribute('href')).scrollIntoView({
        behavior: 'smooth'
      });
    });
  });
</script>
</body>
</html>
