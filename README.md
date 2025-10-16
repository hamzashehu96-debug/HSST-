<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Hamza Shehu School of Technology (HSST)</title>
<style>
/* ===== General Styles ===== */
* {margin:0; padding:0; box-sizing:border-box; font-family:'Poppins', sans-serif;}
body {background:#f6fff6; color:#222; scroll-behavior:smooth;}
a {text-decoration:none;}
h2 {margin-bottom:20px;}
section {padding:80px 20px; opacity:0; transform: translateY(30px); transition: all 1s ease;}
section.active {opacity:1; transform: translateY(0);}

/* ===== Header ===== */
header {
  background: linear-gradient(90deg, #00A884, #0096FF);
  color: white;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 50px;
  position: sticky;
  top: 0;
  z-index: 1000;
  box-shadow: 0 2px 6px rgba(0,0,0,0.15);
  flex-wrap: wrap;
}
.logo {font-size:26px;font-weight:700;letter-spacing:2px;}
nav ul {display:flex; list-style:none; gap:25px;}
nav a {color:white; font-weight:500; transition:0.3s;}
nav a:hover {color:#C8FFB7;}
.apply-btn {
  background:#C8FFB7; color:#1E293B; padding:8px 20px; border-radius:25px; font-weight:600; transition:0.3s;
}
.apply-btn:hover {background:white; color:#00A884; transform:translateY(-2px);}
.menu-toggle {display:none; font-size:28px; cursor:pointer;}
@media(max-width:768px){
  nav ul {display:none; flex-direction:column; width:100%; background:#0096FF; position:absolute; top:60px; left:0; padding:20px 0; text-align:center;}
  nav.active ul {display:flex;}
  .menu-toggle {display:block; color:white;}
  .apply-btn {display:none;}
}

/* ===== Hero ===== */
.hero {height:100vh; display:flex; justify-content:center; align-items:center; text-align:center; color:white;
background: linear-gradient(270deg, #00A884, #0096FF, #C8FFB7); background-size:600% 600%; animation:gradientMove 12s ease infinite; padding:20px;}
@keyframes gradientMove {0%{background-position:0% 50%;}50%{background-position:100% 50%;}100%{background-position:0% 50%;}}
.hero-content h1{font-size:2.5em;margin-bottom:15px;font-weight:700;line-height:1.3; animation:fadeInDown 1s ease forwards;}
.motto{font-size:1.3em;font-style:italic;color:#C8FFB7;margin-bottom:20px; animation:fadeIn 1.5s ease forwards;}
.intro{max-width:700px;margin:0 auto 25px;color:#F9FAFB; animation:fadeIn 2s ease forwards;}
.hero-btn{background:white;color:#0096FF;padding:12px 28px;border-radius:30px;font-weight:600;transition:0.4s;box-shadow:0 4px 10px rgba(0,0,0,0.2);}
.hero-btn:hover{background:#C8FFB7;color:#1E293B;transform:translateY(-3px);}

@keyframes fadeInDown {0%{opacity:0; transform:translateY(-20px);}100%{opacity:1; transform:translateY(0);}}
@keyframes fadeIn {0%{opacity:0;}100%{opacity:1;}}

/* ===== About ===== */
.about {background:#F9FAFB; text-align:center; color:#1E293B;}
.about h2 {font-size:2em; color:#0096FF; margin-bottom:10px;}
.about-intro {max-width:800px;margin:0 auto 50px;font-size:1.1em;color:#334155;}
.about-cards {display:grid; grid-template-columns:repeat(auto-fit,minmax(280px,1fr)); gap:30px; justify-content:center; align-items:stretch;}
.card {background:white; border-radius:20px; padding:30px; box-shadow:0 5px 15px rgba(0,0,0,0.1); transition: transform 0.4s ease, box-shadow 0.4s ease;}
.card:hover {transform:translateY(-8px); box-shadow:0 10px 25px rgba(0,0,0,0.15);}
.icon {font-size:40px; margin-bottom:15px;}
.card h3 {color:#00A884; margin-bottom:10px;}

/* ===== Portals ===== */
.portals {background:linear-gradient(135deg, #E0FBE2, #E6F3FF); text-align:center;}
.portals h2 {font-size:2em; color:#0096FF; margin-bottom:10px;}
.portal-intro {max-width:800px;margin:0 auto 50px;font-size:1.1em;color:#334155;}
.portal-cards {display:grid; grid-template-columns:repeat(auto-fit,minmax(280px,1fr)); gap:30px; justify-content:center;}
.portal-card {background:white; border-radius:20px; padding:30px; box-shadow:0 5px 15px rgba(0,0,0,0.1); transition:transform 0.4s ease, box-shadow 0.4s ease;}
.portal-card:hover {transform:translateY(-10px); box-shadow:0 12px 25px rgba(0,0,0,0.2);}
.portal-icon {font-size:45px; margin-bottom:15px;}
.portal-card h3 {color:#00A884; margin-bottom:10px;}
.portal-btn {display:inline-block;margin-top:15px;background:#0096FF;color:white;padding:10px 25px;border-radius:25px; text-decoration:none; transition:0.3s;}
.portal-btn:hover {background:#00A884;}
.student:hover {border-top:5px solid #00A884;}
.staff:hover {border-top:5px solid #0096FF;}
.admin:hover {border-top:5px solid #C8FFB7;}

/* ===== Admissions ===== */
#admissions {background:#fff7e6;text-align:center;}
#admissions h2 {color:#0096FF;margin-bottom:15px;}
#admissions p {max-width:700px;margin:0 auto 25px;color:#334155;}
#admissions .apply-btn-section {display:inline-block;background:#00A884;color:white;padding:12px 25px;border-radius:30px;font-weight:600;transition:0.3s;}
#admissions .apply-btn-section:hover {background:#C8FFB7;color:#1E293B; transform:translateY(-3px);}

/* ===== News ===== */
#news {background:#F0F8FF;text-align:center;}
#news h2 {color:#0096FF;margin-bottom:20px;}
.news-container {display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr)); gap:20px;}
.news-card {background:white;border-radius:20px;padding:20px;box-shadow:0 5px 15px rgba(0,0,0,0.1);transition:0.3s;}
.news-card:hover {transform:translateY(-5px);}
.news-card h3 {color:#00A884;margin-bottom:10px;}
.news-card p {color:#334155;font-size:0.95em;}

/* ===== Contact ===== */
#contact {background:#e6f9ff;text-align:center;}
#contact h2 {color:#0096FF;margin-bottom:20px;}
.contact-info p {margin-bottom:10px; font-size:1.1em;}
.contact-info a {color:#0096FF;}
.contact-form {max-width:500px;margin:0 auto;}
.contact-form input, .contact-form textarea {width:100%;padding:12px;margin-bottom:15px;border-radius:10px;border:1px solid #ccc;}
.contact-form button {background:#00A884;color:white;padding:12px 25px;border:none;border-radius:25px;font-weight:600;cursor:pointer; transition:0.3s;}
.contact-form button:hover {background:#0096FF;}

/* ===== Footer ===== */
footer {background:#0096FF;color:white;text-align:center;padding:20px;}
footer a {color:white;text-decoration:underline;}
</style>
</head>
<body>

<header>
  <div class="logo">HSST</div>
  <nav id="navbar">
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#portals">Portals</a></li>
      <li><a href="#admissions">Admissions</a></li>
      <li><a href="#news">News</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
  <div class="menu-toggle" id="menu-toggle">&#9776;</div>
  <a href="#admissions" class="apply-btn">Apply Now</a>
</header>

<!-- Hero -->
<section id="home" class="hero">
  <div class="hero-content">
    <h1>Hamza Shehu School of Technology, Faskari (HSST)</h1>
    <p class="motto">"Turning Theoretical Science Into Practical Reality"</p>
    <p class="intro">
      Welcome to HSST -- a modern online and distance-learning institution 
      dedicated to bridging theory with practice through innovative technology education.
    </p>
    <a href="#about" class="hero-btn">Explore HSST</a>
  </div>
</section>

<!-- About -->
<section id="about" class="about">
  <h2>About HSST</h2>
  <p class="about-intro">
    The Hamza Shehu School of Technology, Faskari (HSST) is a private online and distance-learning institution 
    accredited by the NCCE, established in 2025 to transform theoretical science into practical innovation 
    through modern technology education.
  </p>

  <div class="about-cards">
    <div class="card">
      <div class="icon">📘</div>
      <h3>Our History</h3>
      <p>
        Founded in 2025, HSST was built on a vision to bridge the gap between science theory and practical technology.
        It began as a partnership-based institution focused on hands-on computer education.
      </p>
    </div>

    <div class="card">
      <div class="icon">🎯</div>
      <h3>Our Vision</h3>
      <p>
        To become a leading center of excellence in computer and technology education,
        producing graduates who are skilled, innovative, and globally competitive.
      </p>
    </div>

    <div class="card">
      <div class="icon">💡</div>
      <h3>Our Mission</h3>
      <p>
        To provide quality and affordable computer and technology education that bridges theory with practical experience 
        through modern online learning and real-world applications.
      </p>
    </div>
  </div>
</section>

<!-- Portals -->
<section id="portals" class="portals">
  <h2>HSST Portals</h2>
  <p class="portal-intro">
    Access your personalized portal to manage learning, teaching, or administration activities with ease and security.
  </p>

  <div class="portal-cards">
    <div class="portal-card student">
      <div class="portal-icon">👨‍🎓</div>
      <h3>Student Portal</h3>
      <p>View class schedules, assignments, results, and e-learning resources.</p>
      <a href="#" class="portal-btn">Login</a>
    </div>

    <div class="portal-card staff">
      <div class="portal-icon">👩‍🏫</div>
      <h3>Staff Portal</h3>
      <p>Access teaching schedules, upload results, and manage attendance.</p>
      <a href="#" class="portal-btn">Login</a>
    </div>

    <div class="portal-card admin">
      <div class="portal-icon">⚙️</div>
      <h3>Admin Portal</h3>
      <p>Oversee school management, admissions, and performance analytics.</p>
      <a href="#" class="portal-btn">Login</a>
    </div>
  </div>
</section>

<!-- Admissions -->
<section id="admissions" class="admissions">
  <h2>Admissions</h2>
  <p>Apply now to join HSST. Our programs are designed to bridge theory and practice in modern technology education.</p>
  <a href="mailto:hamzashehu96@gmail.com" class="apply-btn-section">Apply Now</a>
</section>

<!-- News & Events -->
<section id="news">
  <h2>News & Events</h2>
  <div class="news-container">
    <div class="news-card">
      <h3>Seminar on AI</h3>
      <p>Join our online seminar on Artificial Intelligence on 20th October 2025 to learn from experts in the field.</p>
    </div>
    <div class="news-card">
      <h3>Student Tech Competition</h3>
      <p>Our annual technology competition is set for November 2025. Showcase your skills and win amazing prizes!</p>
    </div>
    <div class="news-card">
      <h3>New Courses Released</h3>
      <p>We have introduced new online courses in Robotics, IoT, and Data Science. Enroll now!</p>
    </div>
  </div>
</section>

<!-- Contact -->
<section id="contact">
  <h2>Contact Us</h2>
  <div class="contact-info">
    <p>Phone: 07088664478 | 08064749272</p>
    <p>Email: <a href="mailto:hamzashehu96@gmail.com">hamzashehu96@gmail.com</a></p>
  </div>
  <div class="contact-form">
    <input type="text" placeholder="Your Name">
    <input type="email" placeholder="Your Email">
    <textarea placeholder="Your Message" rows="5"></textarea>
    <button>Send Message</button>
  </div>
</section>

<!-- Footer -->
<footer>
  <p>&copy; 2025 Hamza Shehu School of Technology, Faskari (HSST). All rights reserved.</p>
  <p>Designed with ❤️ for modern education</p>
</footer>

<!-- JavaScript -->
<script>
const menuToggle = document.getElementById("menu-toggle");
const navbar = document.getElementById("navbar");
menuToggle.addEventListener("click", () => { navbar.classList.toggle("active"); });

// Scroll animation
const sections = document.querySelectorAll('section');
const scrollAnim = () => {
  const triggerBottom = window.innerHeight / 1.1;
  sections.forEach(section => {
    const sectionTop = section.getBoundingClientRect().top;
    if(sectionTop < triggerBottom){
      section.classList.add('active');
    }
  });
};
window.addEventListener('scroll', scrollAnim);
window.addEventListener('load', scrollAnim);
</script>

</body>
</html>
