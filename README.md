<!doctype doctype>
<html lang="en">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Gopika Mrunalini - Cyber Networking Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&amp;display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
      height: 100%;
    }

    body {
      font-family: 'Poppins', sans-serif;
      color: #fff;
      overflow-x: hidden;
      background: #0a0015;
      height: 100%;
    }

    /* Animated Star Background */
    #starCanvas {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: -1;
      background: linear-gradient(135deg, #1a0033 0%, #0a0015 50%, #2d1b4e 100%);
    }

    /* Navigation */
    nav {
      position: fixed;
      top: 0;
      width: 100%;
      background: rgba(10, 0, 21, 0.9);
      backdrop-filter: blur(10px);
      padding: 1.25rem 0;
      z-index: 1000;
      border-bottom: 1px solid rgba(255, 105, 180, 0.3);
    }

    nav .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    nav .logo {
      font-size: 1.5rem;
      font-weight: 700;
      background: linear-gradient(135deg, #ff69b4, #ffd700);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    nav ul {
      display: flex;
      list-style: none;
      gap: 2rem;
    }

    nav a {
      color: #fff;
      text-decoration: none;
      font-weight: 500;
      transition: all 0.3s ease;
      position: relative;
    }

    nav a:hover {
      color: #ff69b4;
      text-shadow: 0 0 10px rgba(255, 105, 180, 0.8);
    }

    /* Hero Section */
    .hero {
      min-height: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 6rem 2rem 4rem;
      position: relative;
    }

    .hero-content h1 {
      font-size: 3.5rem;
      font-weight: 700;
      margin-bottom: 1rem;
      background: linear-gradient(135deg, #ff69b4, #ffd700, #da70d6);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      animation: glow 2s ease-in-out infinite alternate;
    }

    @keyframes glow {
      from {
        filter: drop-shadow(0 0 10px rgba(255, 105, 180, 0.5));
      }
      to {
        filter: drop-shadow(0 0 20px rgba(255, 215, 0, 0.8));
      }
    }

    .hero-content h2 {
      font-size: 1.75rem;
      font-weight: 400;
      margin-bottom: 2.5rem;
      color: #da70d6;
    }

    .hero-buttons {
      display: flex;
      gap: 1.5rem;
      justify-content: center;
      flex-wrap: wrap;
    }

    .btn {
      padding: 1rem 2.5rem;
      border: none;
      border-radius: 50px;
      font-size: 1.125rem;
      font-weight: 600;
      cursor: pointer;
      transition: all 0.3s ease;
      text-decoration: none;
      display: inline-block;
      position: relative;
      overflow: hidden;
    }

    .btn-primary {
      background: linear-gradient(135deg, #ff69b4, #ffd700);
      color: #0a0015;
      box-shadow: 0 0 20px rgba(255, 105, 180, 0.5);
    }

    .btn-primary:hover {
      transform: translateY(-3px);
      box-shadow: 0 0 30px rgba(255, 215, 0, 0.8), 0 0 50px rgba(255, 105, 180, 0.6);
    }

    .btn-secondary {
      background: transparent;
      color: #fff;
      border: 2px solid #ff69b4;
      box-shadow: 0 0 15px rgba(255, 105, 180, 0.3);
    }

    .btn-secondary:hover {
      background: rgba(255, 105, 180, 0.2);
      border-color: #ffd700;
      box-shadow: 0 0 25px rgba(255, 215, 0, 0.6);
      transform: translateY(-3px);
    }

    /* About Section */
    .about {
      padding: 6rem 2rem;
      background: linear-gradient(135deg, #1a1a1a 0%, #2d2d2d 100%);
      position: relative;
    }

    .about::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: linear-gradient(135deg, rgba(255, 105, 180, 0.1), rgba(255, 215, 0, 0.1));
      pointer-events: none;
    }

    .container {
      max-width: 1200px;
      margin: 0 auto;
      position: relative;
      z-index: 1;
    }

    .section-title {
      font-size: 2.75rem;
      text-align: center;
      margin-bottom: 3rem;
      background: linear-gradient(135deg, #ff69b4, #ffd700);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .about-content {
      display: grid;
      grid-template-columns: 1fr 2fr;
      gap: 3rem;
      align-items: center;
    }

    .profile-image {
      width: 100%;
      max-width: 300px;
      height: 300px;
      border-radius: 50%;
      background: linear-gradient(135deg, #ff69b4, #ffd700);
      padding: 5px;
      margin: 0 auto;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 0 30px rgba(255, 105, 180, 0.5);
    }

    .profile-image-inner {
      width: 100%;
      height: 100%;
      border-radius: 50%;
      background: #2d2d2d;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 5rem;
      filter: grayscale(100%);
    }

    .about-text {
      color: #e0e0e0;
    }

    .about-text h3 {
      font-size: 2rem;
      margin-bottom: 1.25rem;
      color: #fff;
    }

    .about-text p {
      font-size: 1.125rem;
      line-height: 1.8;
      margin-bottom: 1rem;
    }

    /* Skills Section */
    .skills {
      padding: 6rem 2rem;
      background: rgba(10, 0, 21, 0.8);
    }

    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 1.5rem;
      margin-top: 3rem;
    }

    .skill-tag {
      background: rgba(255, 105, 180, 0.1);
      border: 2px solid rgba(255, 105, 180, 0.3);
      padding: 1rem 1.5rem;
      border-radius: 50px;
      text-align: center;
      font-weight: 600;
      transition: all 0.3s ease;
      cursor: pointer;
    }

    .skill-tag:hover {
      background: rgba(255, 105, 180, 0.2);
      border-color: #ffd700;
      transform: translateY(-5px);
      box-shadow: 0 0 20px rgba(255, 215, 0, 0.5);
    }

    /* Projects Section */
    .projects {
      padding: 6rem 2rem;
      background: rgba(10, 0, 21, 0.6);
    }

    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2.5rem;
      margin-top: 3rem;
    }

    .project-card {
      background: rgba(255, 105, 180, 0.05);
      border: 2px solid rgba(255, 105, 180, 0.2);
      border-radius: 20px;
      padding: 2rem;
      transition: all 0.3s ease;
      cursor: pointer;
    }

    .project-card:hover {
      transform: translateY(-10px);
      border-color: #ffd700;
      box-shadow: 0 0 30px rgba(255, 215, 0, 0.4), 0 0 50px rgba(255, 105, 180, 0.3);
      background: rgba(255, 105, 180, 0.1);
    }

    .project-card h3 {
      font-size: 1.75rem;
      margin-bottom: 1rem;
      color: #ff69b4;
    }

    .project-card p {
      font-size: 1.0625rem;
      line-height: 1.6;
      margin-bottom: 1.5rem;
      color: #e0e0e0;
    }

    /* Contact Section */
    .contact {
      padding: 6rem 2rem;
      background: rgba(10, 0, 21, 0.8);
    }

    .contact-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2rem;
      margin-top: 3rem;
    }

    .contact-card {
      background: rgba(255, 105, 180, 0.05);
      border: 2px solid rgba(255, 105, 180, 0.2);
      border-radius: 15px;
      padding: 2rem;
      text-align: center;
      transition: all 0.3s ease;
    }

    .contact-card:hover {
      border-color: #ffd700;
      box-shadow: 0 0 25px rgba(255, 215, 0, 0.4);
      transform: translateY(-5px);
    }

    .contact-card h3 {
      font-size: 1.5rem;
      margin-bottom: 1rem;
      color: #ff69b4;
    }

    .contact-card a {
      color: #da70d6;
      text-decoration: none;
      font-size: 1.0625rem;
      transition: all 0.3s ease;
    }

    .contact-card a:hover {
      color: #ffd700;
      text-shadow: 0 0 10px rgba(255, 215, 0, 0.6);
    }

    /* Footer */
    footer {
      background: rgba(10, 0, 21, 0.95);
      padding: 2rem;
      text-align: center;
      border-top: 2px solid rgba(255, 105, 180, 0.3);
    }

    footer p {
      color: #da70d6;
      font-size: 1.0625rem;
    }

    /* Responsive Design */
    @media (max-width: 768px) {
      nav ul {
        gap: 1rem;
      }

      .hero-content h1 {
        font-size: 2.5rem;
      }

      .hero-content h2 {
        font-size: 1.25rem;
      }

      .about-content {
        grid-template-columns: 1fr;
        text-align: center;
      }

      .section-title {
        font-size: 2rem;
      }
    }
  </style>
  <style>@view-transition { navigation: auto; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
  <script src="/_sdk/element_sdk.js" type="text/javascript"></script>
  <script src="https://cdn.tailwindcss.com" type="text/javascript"></script>
 </head>
 <body><!-- Animated Star Background -->
  <canvas id="starCanvas"></canvas><!-- Navigation -->
  <nav>
   <div class="container">
    <div class="logo">
     GM
    </div>
    <ul>
     <li><a href="#home">Home</a></li>
     <li><a href="#about">About</a></li>
     <li><a href="#skills">Skills</a></li>
     <li><a href="#projects">Projects</a></li>
     <li><a href="#contact">Contact</a></li>
    </ul>
   </div>
  </nav><!-- Hero Section -->
  <section id="home" class="hero">
   <div class="hero-content">
    <h1>Building Secure Networks &amp; Exploring Cyber Defense</h1>
    <h2>Gopika Mrunalini — Cyber Networking Enthusiast &amp; Security Learner</h2>
    <div class="hero-buttons"><a href="#projects" class="btn btn-primary">✨ View Projects ✨</a> <a href="#contact" class="btn btn-secondary">⭐ Contact Me ⭐</a>
    </div>
   </div>
  </section><!-- About Section -->
  <section id="about" class="about">
   <div class="container">
    <h2 class="section-title">About Me</h2>
    <div class="about-content">
     <div class="profile-image">
      <div class="profile-image-inner">
       👩‍💻
      </div>
     </div>
     <div class="about-text">
      <h3>Hello! I'm Gopika Mrunalini</h3>
      <p>I'm a passionate Cyber Networking student with a deep interest in network security, ethical hacking, and digital forensics. My journey in cybersecurity began with a fascination for how networks communicate and how to protect them from threats.</p>
      <p>I specialize in analyzing network traffic, implementing security protocols, and developing tools to enhance network defense. My goal is to become a skilled security professional who can help organizations build resilient and secure network infrastructures.</p>
      <p>When I'm not diving into packet captures or configuring firewalls, I enjoy learning about the latest cybersecurity trends and participating in capture-the-flag competitions.</p>
     </div>
    </div>
   </div>
  </section><!-- Skills Section -->
  <section id="skills" class="skills">
   <div class="container">
    <h2 class="section-title">Technical Skills</h2>
    <div class="skills-grid">
     <div class="skill-tag">
      🌐 TCP/IP
     </div>
     <div class="skill-tag">
      🔧 Subnetting
     </div>
     <div class="skill-tag">
      🦈 Wireshark
     </div>
     <div class="skill-tag">
      🛡 IDS/IPS
     </div>
     <div class="skill-tag">
      🐧 Linux
     </div>
     <div class="skill-tag">
      🐍 Python Scripting
     </div>
     <div class="skill-tag">
      🔐 Network Security Tools
     </div>
     <div class="skill-tag">
      🔥 Firewall Configuration
     </div>
     <div class="skill-tag">
      🕵 Ethical Hacking
     </div>
     <div class="skill-tag">
      📊 Network Analysis
     </div>
     <div class="skill-tag">
      🔒 Cryptography
     </div>
     <div class="skill-tag">
      ⚡ Penetration Testing
     </div>
    </div>
   </div>
  </section><!-- Projects Section -->
  <section id="projects" class="projects">
   <div class="container">
    <h2 class="section-title">Featured Projects</h2>
    <div class="projects-grid">
     <div class="project-card">
      <h3>🌐 VLAN Segmentation Lab</h3>
      <p>Designed and implemented a multi-VLAN network environment to enhance security through network segmentation. Configured inter-VLAN routing and access control lists to manage traffic flow between different network segments.</p><a href="#" class="btn btn-secondary">View Details</a>
     </div>
     <div class="project-card">
      <h3>🦈 Wireshark Packet Analysis</h3>
      <p>Conducted comprehensive network traffic analysis using Wireshark to identify security vulnerabilities and suspicious activities. Created detailed reports on protocol behaviors and potential attack vectors.</p><a href="#" class="btn btn-secondary">View Details</a>
     </div>
     <div class="project-card">
      <h3>🐍 Python Network Scanner</h3>
      <p>Developed a custom network scanning tool in Python to discover active hosts, open ports, and running services. Implemented multi-threading for efficient scanning and generated comprehensive security reports.</p><a href="#" class="btn btn-secondary">GitHub</a>
     </div>
     <div class="project-card">
      <h3>🔥 Firewall Configuration Project</h3>
      <p>Configured and optimized enterprise-grade firewall rules to protect network infrastructure. Implemented zone-based security policies and created comprehensive documentation for security best practices.</p><a href="#" class="btn btn-secondary">View Details</a>
     </div>
    </div>
   </div>
  </section><!-- Contact Section -->
  <section id="contact" class="contact">
   <div class="container">
    <h2 class="section-title">Get In Touch</h2>
    <div class="contact-grid">
     <div class="contact-card">
      <h3>📧 Email</h3><a href="mailto:gopika.mrunalini@example.com">gopika.mrunalini@example.com</a>
     </div>
     <div class="contact-card">
      <h3>💼 LinkedIn</h3><a href="https://linkedin.com" target="_blank" rel="noopener noreferrer">Connect with me</a>
     </div>
     <div class="contact-card">
      <h3>💻 GitHub</h3><a href="https://github.com" target="_blank" rel="noopener noreferrer">View my repositories</a>
     </div>
    </div>
   </div>
  </section><!-- Footer -->
  <footer>
   <p>© 2025 Gopika Mrunalini • Cyber Networking Portfolio</p>
  </footer>
  <script>
    // Animated Star Background with Mouse Interaction
    const canvas = document.getElementById('starCanvas');
    const ctx = canvas.getContext('2d');
    
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;

    let mouseX = 0;
    let mouseY = 0;

    class Star {
      constructor() {
        this.x = Math.random() * canvas.width;
        this.y = Math.random() * canvas.height;
        this.size = Math.random() * 2 + 0.5;
        this.speedX = (Math.random() - 0.5) * 0.5;
        this.speedY = (Math.random() - 0.5) * 0.5;
        this.color = this.getRandomColor();
        this.pulseSpeed = Math.random() * 0.02 + 0.01;
        this.pulsePhase = Math.random() * Math.PI * 2;
      }

      getRandomColor() {
        const colors = [
          'rgba(255, 105, 180, ',  // Pink
          'rgba(255, 215, 0, ',     // Gold
          'rgba(218, 112, 214, ',   // Violet
          'rgba(255, 182, 193, '    // Light Pink
        ];
        return colors[Math.floor(Math.random() * colors.length)];
      }

      update() {
        this.x += this.speedX;
        this.y += this.speedY;

        // Mouse interaction
        const dx = mouseX - this.x;
        const dy = mouseY - this.y;
        const distance = Math.sqrt(dx * dx + dy * dy);
        
        if (distance < 150) {
          const force = (150 - distance) / 150;
          this.x -= dx * force * 0.03;
          this.y -= dy * force * 0.03;
        }

        // Wrap around screen
        if (this.x < 0) this.x = canvas.width;
        if (this.x > canvas.width) this.x = 0;
        if (this.y < 0) this.y = canvas.height;
        if (this.y > canvas.height) this.y = 0;

        this.pulsePhase += this.pulseSpeed;
      }

      draw() {
        const pulse = Math.sin(this.pulsePhase) * 0.5 + 0.5;
        const alpha = 0.3 + pulse * 0.7;
        
        ctx.fillStyle = this.color + alpha + ')';
        ctx.shadowBlur = 10 + pulse * 10;
        ctx.shadowColor = this.color + '0.8)';
        
        ctx.beginPath();
        ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
        ctx.fill();
      }
    }

    // Create stars
    const stars = [];
    for (let i = 0; i < 200; i++) {
      stars.push(new Star());
    }

    // Animation loop
    function animate() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);
      
      stars.forEach(star => {
        star.update();
        star.draw();
      });

      requestAnimationFrame(animate);
    }

    animate();

    // Mouse tracking
    document.addEventListener('mousemove', (e) => {
      mouseX = e.clientX;
      mouseY = e.clientY;
    });

    // Resize canvas
    window.addEventListener('resize', () => {
      canvas.width = window.innerWidth;
      canvas.height = window.innerHeight;
    });

    // Smooth scroll for navigation links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
          target.scrollIntoView({
            behavior: 'smooth',
            block: 'start'
          });
        }
      });
    });
  </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'99abf3c5a21bb294',t:'MTc2MjUwOTI5Ny4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
