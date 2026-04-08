<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Nandini Prajapati · Backend Engineer README</title>
  <!-- Google Fonts + Fira Code for monospace -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&family=Fira+Code:wght@400;500;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #0a0c10;
      font-family: 'Inter', 'Fira Code', monospace, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 2rem 1.5rem;
    }

    /* main readme container — exactly like GitHub profile but refined */
    .readme-container {
      max-width: 1100px;
      width: 100%;
      background: #0d1117;
      border-radius: 32px;
      box-shadow: 0 25px 45px -12px rgba(0, 247, 255, 0.2), 0 0 0 1px rgba(0, 247, 255, 0.15);
      padding: 2rem 2rem 2.5rem 2rem;
      transition: all 0.2s;
    }

    h1 {
      font-size: 2.8rem;
      font-weight: 800;
      background: linear-gradient(135deg, #FFFFFF 20%, #00F7FF 85%);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      letter-spacing: -0.5px;
      margin-bottom: 0.5rem;
    }

    /* Separator styling */
    .section-divider {
      margin: 2rem 0 1.8rem 0;
      border: none;
      height: 2px;
      background: linear-gradient(90deg, #00F7FF, transparent);
    }

    /* about + connect side-by-side (separate sections) */
    .info-split {
      display: flex;
      flex-wrap: wrap;
      gap: 2rem;
      margin: 2rem 0 1.5rem 0;
    }

    .about-box {
      flex: 2;
      min-width: 240px;
      background: rgba(0, 247, 255, 0.02);
      border-radius: 28px;
      padding: 1.5rem 1.8rem;
      border: 1px solid rgba(0, 247, 255, 0.2);
      backdrop-filter: blur(2px);
    }

    .connect-box {
      flex: 1.2;
      min-width: 220px;
      background: rgba(0, 247, 255, 0.02);
      border-radius: 28px;
      padding: 1.5rem 1.8rem;
      border: 1px solid rgba(0, 247, 255, 0.2);
      backdrop-filter: blur(2px);
    }

    .section-title {
      font-size: 1.6rem;
      font-weight: 700;
      margin-bottom: 1.2rem;
      display: inline-block;
      background: linear-gradient(120deg, #e0f2fe, #00F7FF);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      border-left: 4px solid #00F7FF;
      padding-left: 0.8rem;
    }

    .about-text {
      font-size: 1rem;
      color: #c9d1d9;
      line-height: 1.6;
    }

    .about-text b {
      color: #00F7FF;
      font-weight: 700;
    }

    .about-text i {
      color: #8b949e;
    }

    .connect-links {
      display: flex;
      flex-direction: column;
      gap: 1rem;
      margin-top: 0.5rem;
    }

    .connect-item {
      display: flex;
      align-items: center;
      gap: 12px;
      font-size: 1rem;
      transition: transform 0.2s ease;
    }

    .connect-item a {
      text-decoration: none;
      color: #e6edf3;
      font-weight: 500;
      transition: all 0.2s;
      display: inline-flex;
      align-items: center;
      gap: 8px;
    }

    .connect-item a i {
      width: 28px;
      font-size: 1.4rem;
      transition: 0.2s;
    }

    .connect-item a:hover {
      color: #00F7FF;
      transform: translateX(6px);
    }

    .connect-item a:hover i {
      color: #00F7FF;
      text-shadow: 0 0 4px #00F7FF;
    }

    /* Bold & Attractive Typing Animation */
    .typing-section {
      background: rgba(0, 247, 255, 0.04);
      border-radius: 40px;
      padding: 0.9rem 1.6rem;
      margin: 1.8rem 0 1rem 0;
      border: 1px solid rgba(0, 247, 255, 0.3);
      box-shadow: 0 8px 20px rgba(0,0,0,0.4);
    }

    .typing-container {
      display: flex;
      justify-content: center;
      align-items: baseline;
      flex-wrap: wrap;
      gap: 0.4rem;
    }

    .static-greeting {
      font-family: 'Fira Code', monospace;
      font-weight: 800;
      font-size: 1.8rem;
      background: linear-gradient(125deg, #ffffff, #9effff);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      letter-spacing: -0.5px;
    }

    .typed-words {
      font-family: 'Fira Code', monospace;
      font-weight: 800;
      font-size: 1.9rem;
      background: linear-gradient(135deg, #00F7FF, #6efff0);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      text-shadow: 0 0 6px rgba(0,247,255,0.4);
      position: relative;
    }

    .typed-cursor {
      font-size: 2rem;
      font-weight: 800;
      color: #00F7FF;
      text-shadow: 0 0 5px #00F7FF;
      animation: blink 0.9s step-end infinite;
      margin-left: 3px;
    }

    @keyframes blink {
      0%, 100% { opacity: 1; }
      50% { opacity: 0; }
    }

    /* Tech stack layout same as original but crisp */
    .tech-section {
      margin: 2rem 0;
    }
    .tech-title {
      font-size: 1.5rem;
      font-weight: 700;
      margin-bottom: 1rem;
      color: #e6edf3;
      letter-spacing: -0.3px;
      display: flex;
      align-items: center;
      gap: 10px;
    }
    .tech-title i {
      color: #00F7FF;
    }
    .skills-panel {
      background: #0d1117;
      border-radius: 24px;
      padding: 1rem 0 0.5rem 0;
    }
    .skill-icons {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      margin: 0.8rem 0;
    }
    .skill-icons img {
      transition: transform 0.2s;
    }
    .skill-icons img:hover {
      transform: translateY(-5px);
    }

    /* GitHub Stats */
    .stats-row {
      display: flex;
      flex-wrap: wrap;
      gap: 1.5rem;
      margin: 2rem 0 1rem;
      justify-content: center;
    }
    .stats-card {
      background: rgba(13, 17, 23, 0.8);
      border-radius: 20px;
      padding: 0.5rem;
      transition: all 0.2s;
      border: 1px solid #21262d;
    }
    .stats-card img {
      width: 100%;
      max-width: 460px;
      border-radius: 16px;
    }

    /* Responsive */
    @media (max-width: 760px) {
      .readme-container {
        padding: 1.5rem;
      }
      h1 { font-size: 2rem; }
      .static-greeting, .typed-words {
        font-size: 1.2rem;
      }
      .typed-cursor { font-size: 1.4rem; }
      .about-box, .connect-box {
        padding: 1.2rem;
      }
      .section-title {
        font-size: 1.3rem;
      }
    }
    hr {
      border: 0;
      height: 1px;
      background: #21262d;
      margin: 1rem 0;
    }
    .footer-note {
      text-align: center;
      color: #6e7681;
      font-size: 0.8rem;
      margin-top: 2rem;
    }
  </style>
</head>
<body>
<div class="readme-container">
  
  <!-- Main Heading -->
  <h1 align="center">Hi 👋, I'm Nandini Prajapati</h1>
  <h3 align="center" style="color:#8b949e; font-weight: 500; margin-top: -8px;">🚀 Backend Developer | Computer Science Student</h3>
  
  <!-- BOLD + ATTRACTIVE TYPING ANIMATION (Enhanced version) -->
  <div class="typing-section">
    <div class="typing-container">
      <span class="static-greeting">⚡&nbsp;</span>
      <span class="typed-words" id="typed-output"></span>
      <span class="typed-cursor">|</span>
    </div>
  </div>
  
  <!-- SEPARATE ABOUT & CONNECT SECTION (next to each other but distinct) -->
  <div class="info-split">
    <!-- ABOUT ME section (separate) -->
    <div class="about-box">
      <div class="section-title">
        <i class="fas fa-user-astronaut" style="margin-right: 8px;"></i> About
      </div>
      <div class="about-text">
        💻 <b>CS Student & Backend Developer</b><br><br>
        ⚙️ Building <b>Scalable APIs & Systems</b><br>
        🌱 <b>Node.js, Express.js, MongoDB</b><br>
        🎯 Focus: <b>High-performance Backend Architecture</b><br>
        🔥 Clean code advocate & always innovating.<br><br>
        <i>“Crafting robust backend solutions with modern stacks.”</i>
      </div>
    </div>
    
    <!-- CONNECT section (completely separate, right side) -->
    <div class="connect-box">
      <div class="section-title">
        <i class="fas fa-plug"></i> Connect
      </div>
      <div class="connect-links">
        <div class="connect-item">
          <a href="mailto:bp623989@gmail.com" target="_blank">
            <i class="fas fa-envelope" style="color:#EA4335;"></i> bp623989@gmail.com
          </a>
        </div>
        <div class="connect-item">
          <a href="https://www.linkedin.com/in/nandini-prajapati-6351363b1/" target="_blank">
            <i class="fab fa-linkedin" style="color:#0A66C2;"></i> LinkedIn
          </a>
        </div>
        <div class="connect-item">
          <a href="https://x.com/NandiniPraj4434" target="_blank">
            <i class="fab fa-twitter" style="color:#1DA1F2;"></i> Twitter / X
          </a>
        </div>
        <div class="connect-item">
          <a href="https://www.youtube.com/@NandiniPrajapati-n8z" target="_blank">
            <i class="fab fa-youtube" style="color:#FF0000;"></i> YouTube
          </a>
        </div>
        <div class="connect-item">
          <a href="https://github.com/YOUR_GITHUB_USERNAME" target="_blank">
            <i class="fab fa-github" style="color:#ffffff;"></i> GitHub
          </a>
        </div>
      </div>
    </div>
  </div>
  
  <!-- tech stack section -->
  <div class="tech-section">
    <div class="tech-title">
      <i class="fas fa-cogs"></i> 🛠️ Tech Stack
    </div>
    
    <!-- Backend -->
    <div style="margin-bottom: 1.2rem;">
      <span style="color:#c9d1d9; font-weight: 600;">⚙️ Backend Development</span>
      <div class="skill-icons">
        <img src="https://skillicons.dev/icons?i=nodejs,express,mongodb,cpp&theme=dark" alt="backend icons" />
      </div>
    </div>
    
    <!-- Frontend -->
    <div style="margin-bottom: 1.2rem;">
      <span style="color:#c9d1d9; font-weight: 600;">🚀 Frontend Development</span>
      <div class="skill-icons">
        <img src="https://skillicons.dev/icons?i=html,css,js,react&theme=dark" alt="frontend icons" />
      </div>
    </div>
    
    <!-- Tools -->
    <div>
      <span style="color:#c9d1d9; font-weight: 600;">🧰 Tools & Version Control</span>
      <div class="skill-icons">
        <img src="https://skillicons.dev/icons?i=git,postman,vscode&theme=dark" alt="tools icons" />
      </div>
    </div>
    
    <!-- additional techstack generator SVG (like original but improved) -->
    <div align="center" style="margin-top: 1.2rem;">
      <img src="https://techstack-generator.vercel.app/rest-api-skills.svg?lang=en&skills=nodejs,express,mongodb,cpp,react,html5,css3,javascript,git,postman,vscode&background=000000" width="100%" alt="tech stack generator" />
    </div>
  </div>
  
  <!-- GitHub Stats Section exactly as requested style -->
  <div class="stats-row">
    <div class="stats-card">
      <img src="https://github-readme-stats.vercel.app/api?username=YOUR_GITHUB_USERNAME&show_icons=true&theme=tokyonight&hide_border=true" alt="GitHub Stats" />
    </div>
    <div class="stats-card">
      <img src="https://github-readme-streak-stats.herokuapp.com/?user=YOUR_GITHUB_USERNAME&theme=tokyonight&hide_border=true" alt="GitHub Streak" />
    </div>
  </div>
  
  <hr class="section-divider" />
  <div class="footer-note">
    ⚡ Backend Architect · Node.js Expert · Scalable Infrastructure
  </div>
</div>

<!-- Typing Animation Script: BOLD, ATTRACTIVE, MULTI-LINE (modern) -->
<script>
  (function() {
    // list of powerful, bold statements for the typing effect
    const phrases = [
      "BACKEND ARCHITECT",
      "NODE.JS EXPERT",
      "SCALABLE INFRASTRUCTURE",
      "CLEAN CODE PRACTITIONER",
      "ALWAYS INNOVATING"
    ];
    
    let index = 0;
    let charIndex = 0;
    let currentPhrase = phrases[0];
    let isDeleting = false;
    const typedElement = document.getElementById('typed-output');
    
    function typeEffect() {
      if (!typedElement) return;
      
      const fullText = currentPhrase;
      let displayedText = '';
      
      if (isDeleting) {
        // remove characters
        displayedText = fullText.substring(0, charIndex - 1);
        charIndex--;
      } else {
        // add characters
        displayedText = fullText.substring(0, charIndex + 1);
        charIndex++;
      }
      
      typedElement.innerText = displayedText;
      
      // determine speed and next steps
      let typingSpeed = isDeleting ? 50 : 90;
      
      if (!isDeleting && charIndex === fullText.length) {
        // finished typing a phrase: pause before deleting
        typingSpeed = 1800;
        isDeleting = true;
      } else if (isDeleting && charIndex === 0) {
        // finished deleting: move to next phrase
        isDeleting = false;
        index = (index + 1) % phrases.length;
        currentPhrase = phrases[index];
        typingSpeed = 200;
      }
      
      setTimeout(typeEffect, typingSpeed);
    }
    
    // start typing animation after page loads
    setTimeout(() => {
      typeEffect();
    }, 300);
  })();
</script>

<!-- Optional note: The GitHub stats show placeholder username. Replace "YOUR_GITHUB_USERNAME" with actual GitHub username for real stats -->
</body>
</html>
