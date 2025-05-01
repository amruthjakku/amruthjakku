<!-- COSMIC NEBULIX THEME: Advanced animated GitHub profile with 3D effects and interactive elements -->

<style>
  /* Base styling */
  body {
    font-family: 'Inter', sans-serif;
    background: linear-gradient(to bottom, #0d1117, #161b22);
    color: #fff;
    margin: 0;
    padding: 0;
    overflow-x: hidden;
  }
  
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
  }
  
  /* Cosmic animations */
  @keyframes float {
    0% { transform: translateY(0px); }
    50% { transform: translateY(-20px); }
    100% { transform: translateY(0px); }
  }
  
  @keyframes pulse {
    0% { transform: scale(1); opacity: 1; }
    50% { transform: scale(1.05); opacity: 0.8; }
    100% { transform: scale(1); opacity: 1; }
  }
  
  @keyframes shimmer {
    0% { background-position: -100% 0; }
    100% { background-position: 200% 0; }
  }
  
  @keyframes rotate {
    from { transform: rotate(0deg); }
    to { transform: rotate(360deg); }
  }
  
  /* Glassmorphism */
  .glass-card {
    background: rgba(255, 255, 255, 0.05);
    backdrop-filter: blur(10px);
    border-radius: 16px;
    padding: 24px;
    border: 1px solid rgba(255, 255, 255, 0.1);
    box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.2);
    transition: all 0.3s ease;
  }
  
  .glass-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 12px 48px 0 rgba(31, 38, 135, 0.3);
    border: 1px solid rgba(255, 255, 255, 0.2);
  }
  
  /* Gradient animations */
  .gradient-text {
    background: linear-gradient(90deg, #8A2387, #E94057, #F27121, #8A2387);
    background-size: 300% 100%;
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
    animation: shimmer 8s linear infinite;
  }
  
  .cosmic-border {
    position: relative;
    border-radius: 16px;
    overflow: hidden;
  }
  
  .cosmic-border::before {
    content: '';
    position: absolute;
    top: -2px;
    left: -2px;
    right: -2px;
    bottom: -2px;
    background: linear-gradient(45deg, #8A2387, #E94057, #F27121, #8A2387);
    background-size: 400% 400%;
    z-index: -1;
    animation: shimmer 8s linear infinite;
    border-radius: 18px;
  }
  
  /* Progress bars */
  .progress-container {
    background: rgba(255, 255, 255, 0.1);
    border-radius: 10px;
    height: 10px;
    width: 100%;
    margin: 15px 0;
    overflow: hidden;
  }
  
  .progress-bar {
    height: 100%;
    border-radius: 10px;
    background: linear-gradient(90deg, #8A2387, #E94057, #F27121);
    background-size: 200% 100%;
    animation: shimmer 5s linear infinite;
    transition: width 1.5s ease-in-out;
  }
  
  /* Hover effects */
  .hover-lift {
    transition: transform 0.3s ease;
  }
  
  .hover-lift:hover {
    transform: translateY(-5px);
  }
  
  /* Tech badges */
  .tech-badge {
    display: inline-block;
    padding: 5px 10px;
    margin: 5px;
    border-radius: 6px;
    background: rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(5px);
    border: 1px solid rgba(255, 255, 255, 0.1);
    transition: all 0.3s ease;
  }
  
  .tech-badge:hover {
    background: rgba(255, 255, 255, 0.2);
    transform: translateY(-3px);
    box-shadow: 0 7px 15px rgba(0, 0, 0, 0.2);
  }
  
  /* Neon effects */
  .neon {
    text-shadow: 0 0 5px rgba(233, 64, 87, 0.5), 
                 0 0 10px rgba(233, 64, 87, 0.3), 
                 0 0 15px rgba(233, 64, 87, 0.2);
  }
  
  /* 3D card effect */
  .card-3d-container {
    perspective: 1000px;
  }
  
  .card-3d {
    transition: transform 0.5s;
    transform-style: preserve-3d;
  }
  
  .card-3d:hover {
    transform: rotateY(10deg) rotateX(5deg);
  }
  
  /* Pulse animation for elements */
  .pulse {
    animation: pulse 3s ease-in-out infinite;
  }
  
  /* Floating animation */
  .float {
    animation: float 6s ease-in-out infinite;
  }
  
  /* Grid layouts */
  .grid-2 {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
  }
  
  .grid-3 {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
  }
  
  .grid-4 {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 15px;
  }
  
  /* Responsive adjustments */
  @media (max-width: 1024px) {
    .grid-4 {
      grid-template-columns: repeat(3, 1fr);
    }
  }
  
  @media (max-width: 768px) {
    .grid-3, .grid-4 {
      grid-template-columns: repeat(2, 1fr);
    }
  }
  
  @media (max-width: 480px) {
    .grid-2, .grid-3, .grid-4 {
      grid-template-columns: 1fr;
    }
  }
  
  /* Custom cosmic elements */
  .cosmic-sphere {
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background: radial-gradient(circle at 30% 30%, #f27121, #e94057, #8a2387);
    box-shadow: 0 0 20px rgba(233, 64, 87, 0.5), 
                0 0 40px rgba(233, 64, 87, 0.3), 
                0 0 60px rgba(233, 64, 87, 0.2);
    animation: pulse 3s ease-in-out infinite;
  }
  
  .orbit {
    position: relative;
    width: 200px;
    height: 200px;
    border-radius: 50%;
    border: 1px solid rgba(255, 255, 255, 0.1);
    animation: rotate 20s linear infinite;
  }
  
  .planet {
    position: absolute;
    width: 20px;
    height: 20px;
    border-radius: 50%;
    background: #E94057;
    top: 0;
    left: 90px;
    box-shadow: 0 0 10px rgba(233, 64, 87, 0.8);
  }
  
  /* Stats bar with animated loading */
  .stat-bar {
    height: 8px;
    width: 0;
    background: linear-gradient(90deg, #8A2387, #E94057, #F27121);
    border-radius: 4px;
    animation: load-bar 2s ease-out forwards;
  }
  
  @keyframes load-bar {
    0% { width: 0; }
    100% { width: 100%; }
  }
  
  /* Star field background */
  .star-field {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -2;
    overflow: hidden;
  }
  
  .star {
    position: absolute;
    width: 2px;
    height: 2px;
    background: white;
    border-radius: 50%;
    animation: twinkle 5s infinite;
  }
  
  @keyframes twinkle {
    0%, 100% { opacity: 0.2; }
    50% { opacity: 1; }
  }
  
  /* Create 100 stars with random positions */
  .star-field::before {
    content: '';
    position: absolute;
    width: 100%;
    height: 100%;
    background-image: radial-gradient(white 1px, transparent 0);
    background-size: 50px 50px;
    opacity: 0.3;
  }
  
  /* Add a subtle nebula background */
  .nebula-bg {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: radial-gradient(circle at 50% 50%, rgba(233, 64, 87, 0.1), transparent 80%),
                radial-gradient(circle at 80% 20%, rgba(138, 35, 135, 0.1), transparent 60%),
                radial-gradient(circle at 20% 80%, rgba(242, 113, 33, 0.1), transparent 70%);
    z-index: -3;
    filter: blur(60px);
  }
  
  /* Tech experience bars */
  .tech-exp {
    margin-bottom: 15px;
  }
  
  .tech-name {
    display: flex;
    justify-content: space-between;
    margin-bottom: 5px;
  }
  
  /* Subtle parallax effect */
  .parallax {
    transition: transform 0.2s ease-out;
  }
</style>

<!-- Star Field Background -->
<div class="star-field"></div>
<div class="nebula-bg"></div>

<div class="container">
  <!-- HERO SECTION WITH COSMIC ANIMATION -->
  <div align="center" class="cosmic-border">
    <div style="padding: 8px; background: rgba(13, 17, 23, 0.6); border-radius: 16px;">
      <img src="https://capsule-render.vercel.app/api?type=waving&height=300&text=Jakku%20Amruth&fontColor=ffffff&color=0:8A2387,50:E94057,100:F27121&stroke=3A1C71&strokeWidth=3&animation=fadeIn&desc=Innovation%20Architect%20%7C%20AI%20Pioneer%20%7C%20Future%20Builder&descAlignY=70&descSize=18" width="100%" class="pulse"/>
      
      <div class="float">
        <a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=18&pause=1000&color=E94057&center=true&vCenter=true&random=false&width=600&lines=AI+Engineer+⚡+Innovation+Architect+⚡+MS+Candidate;Building+the+future+with+code+✨+data+✨+algorithms;Blending+creativity+with+technical+precision;Pushing+boundaries+of+what's+possible+with+AI" alt="Typing SVG" /></a>
      </div>
      
      <div style="margin: 20px 0;">
        <a href="https://www.linkedin.com/in/amruthjakku/" class="hover-lift"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0077B5" /></a>
        <a href="https://devpost.com/amruthjakku" class="hover-lift"><img src="https://img.shields.io/badge/Devpost-003E54?style=for-the-badge&logo=Devpost&logoColor=white" /></a>
        <a href="mailto:amruthjakku@example.com" class="hover-lift"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>
        <a href="https://yourwebsite.com" class="hover-lift"><img src="https://img.shields.io/badge/Portfolio-6c63ff?style=for-the-badge&logo=About.me&logoColor=white" /></a>
      </div>
    </div>
  </div>
  
  <!-- ANIMATED DIVIDER -->
  <div align="center" style="margin: 30px 0;">
    <img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="rainbow" width="100%">
  </div>
  
  <!-- ABOUT ME SECTION WITH 3D ANIMATION -->
  <div class="card-3d-container">
    <div class="card-3d glass-card" style="margin-bottom: 30px;">
      <div style="display: flex; flex-wrap: wrap; gap: 20px;">
        <div style="flex: 1; min-width: 300px;">
          <h2 class="gradient-text" style="font-size: 28px; font-weight: 700;">🌌 The Vision</h2>
          <p style="line-height: 1.6; font-size: 16px;">Building intelligent systems that transform how we interact with technology. I combine AI, data, and human-centered design to create solutions that solve real problems.</p>
          <p style="line-height: 1.6; font-size: 16px;">My mission is to develop ethical, accessible, and innovative AI that expands human capabilities while promoting safety and inclusion.</p>
          
          <h3 class="neon" style="margin-top: 25px; font-size: 22px;">💫 Current Orbit</h3>
          <div style="display: flex; align-items: center; margin-bottom: 10px;">
            <div class="cosmic-sphere" style="width: 12px; height: 12px; margin-right: 10px;"></div>
            <p style="margin: 0;">MS in AI & Machine Learning (in progress)</p>
          </div>
          <div style="display: flex; align-items: center; margin-bottom: 10px;">
            <div class="cosmic-sphere" style="width: 12px; height: 12px; margin-right: 10px;"></div>
            <p style="margin: 0;">Specializing in LLMs, Computer Vision, and AI Safety</p>
          </div>
          <div style="display: flex; align-items: center;">
            <div class="cosmic-sphere" style="width: 12px; height: 12px; margin-right: 10px;"></div>
            <p style="margin: 0;">Hackathon enthusiast & open-source contributor</p>
          </div>
        </div>
        
        <div style="flex: 1; min-width: 300px; display: flex; justify-content: center; align-items: center;">
          <div class="float">
            <div style="position: relative; width: 280px; height: 280px;">
              <!-- Orbit animations -->
              <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 200px; height: 200px; border-radius: 50%; border: 1px dashed rgba(233, 64, 87, 0.3); animation: rotate 15s linear infinite;"></div>
              <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 150px; height: 150px; border-radius: 50%; border: 1px dashed rgba(138, 35, 135, 0.3); animation: rotate 10s linear infinite reverse;"></div>
              <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 100px; height: 100px; border-radius: 50%; border: 1px dashed rgba(242, 113, 33, 0.3); animation: rotate 5s linear infinite;"></div>
              
              <!-- Central image -->
              <img src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif" style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 80%; height: auto; border-radius: 10px; box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);"/>
              
              <!-- Orbiting elements -->
              <div style="position: absolute; top: 0; left: 50%; transform: translateX(-50%); width: 20px; height: 20px; border-radius: 50%; background: #E94057; box-shadow: 0 0 10px #E94057; animation: pulse 3s infinite;"></div>
              <div style="position: absolute; bottom: 0; left: 50%; transform: translateX(-50%); width: 15px; height: 15px; border-radius: 50%; background: #8A2387; box-shadow: 0 0 10px #8A2387; animation: pulse 4s infinite;"></div>
              <div style="position: absolute; left: 0; top: 50%; transform: translateY(-50%); width: 12px; height: 12px; border-radius: 50%; background: #F27121; box-shadow: 0 0 10px #F27121; animation: pulse 5s infinite;"></div>
              <div style="position: absolute; right: 0; top: 50%; transform: translateY(-50%); width: 18px; height: 18px; border-radius: 50%; background: #4CB8C4; box-shadow: 0 0 10px #4CB8C4; animation: pulse 6s infinite;"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  
  <!-- PROJECT SHOWCASE WITH ANIMATED CARDS -->
  <h2 align="center" class="gradient-text" style="font-size: 32px; margin-bottom: 20px;">🚀 Breakthrough Projects</h2>
  <div align="center" style="margin-bottom: 30px;">
    <img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/solar.png" alt="solar" width="100%">
  </div>
  
  <!-- GLASSMORPHISM PROJECT CARDS WITH HOVER ANIMATIONS -->
  <div class="grid-2">
    <!-- PROJECT 1 -->
    <div class="glass-card cosmic-border parallax" data-depth="0.2">
      <div style="display: flex; justify-content: space-between; align-items: flex-start;">
        <h3 class="gradient-text" style="font-size: 24px; margin: 0;">🚨 CyberBot</h3>
        <div class="cosmic-sphere" style="width: 40px; height: 40px;"></div>
      </div>
      <p style="font-style: italic; margin: 10px 0 20px;"><i>AI-powered cybercrime reporting & analysis system</i></p>
      
      <div style="display: flex; flex-wrap: wrap; gap: 8px; margin: 15px 0;">
        <span class="tech-badge">TensorFlow</span>
        <span class="tech-badge">FastAPI</span>
        <span class="tech-badge">NLP</span>
      </div>
      
      <ul style="padding-left: 20px; line-height: 1.6;">
        <li>94% accuracy in incident classification</li>
        <li>70% reduction in reporting time</li>
        <li>Deployed with law enforcement agencies</li>
      </ul>
      
      <!-- ANIMATED PROGRESS BAR -->
      <div class="progress-container">
        <div class="progress-bar" style="width: 85%;"></div>
      </div>
      <p align="right" style="margin: 5px 0 0;"><b>85% Complete</b></p>
    </div>
    
    <!-- PROJECT 2 -->
    <div class="glass-card cosmic-border parallax" data-depth="0.3">
      <div style="display: flex; justify-content: space-between; align-items: flex-start;">
        <h3 class="gradient-text" style="font-size: 24px; margin: 0;">🛡️ DeepShield</h3>
        <div class="cosmic-sphere" style="width: 40px; height: 40px;"></div>
      </div>
      <p style="font-style: italic; margin: 10px 0 20px;"><i>Advanced deepfake & AI content detection platform</i></p>
      
      <div style="display: flex; flex-wrap: wrap; gap: 8px; margin: 15px 0;">
        <span class="tech-badge">PyTorch</span>
        <span class="tech-badge">OpenCV</span>
        <span class="tech-badge">Computer Vision</span>
      </div>
      
      <ul style="padding-left: 20px; line-height: 1.6;">
        <li>Multi-modal detection system</li>
        <li>Real-time monitoring capabilities</li>
        <li>Featured in AI safety competitions</li>
      </ul>
      
      <!-- ANIMATED PROGRESS BAR -->
      <div class="progress-container">
        <div class="progress-bar" style="width: 73%;"></div>
      </div>
      <p align="right" style="margin: 5px 0 0;"><b>73% Complete</b></p>
    </div>
    
    <!-- PROJECT 3 -->
    <div class="glass-card cosmic-border parallax" data-depth="0.2">
      <div style="display: flex; justify-content: space-between; align-items: flex-start;">
        <h3 class="gradient-text" style="font-size: 24px; margin: 0;">⚖️ CrimeChain</h3>
        <div class="cosmic-sphere" style="width: 40px; height: 40px;"></div>
      </div>
      <p style="font-style: italic; margin: 10px 0 20px;"><i>Blockchain-powered evidence management</i></p>
      
      <div style="display: flex; flex-wrap: wrap; gap: 8px; margin: 15px 0;">
        <span class="tech-badge">Solidity</span>
        <span class="tech-badge">Arweave</span>
        <span class="tech-badge">Web3</span>
      </div>
      
      <ul style="padding-left: 20px; line-height: 1.6;">
        <li>Tamper-proof evidence chain</li>
        <li>60% reduced processing time</li>
        <li>Advanced cryptographic verification</li>
      </ul>
      
      <!-- ANIMATED PROGRESS BAR -->
      <div class="progress-container">
        <div class="progress-bar" style="width: 67%;"></div>
      </div>
      <p align="right" style="margin: 5px 0 0;"><b>67% Complete</b></p>
    </div>
    
    <!-- PROJECT 4 -->
    <div class="glass-card cosmic-border parallax" data-depth="0.3">
      <div style="display: flex; justify-content: space-between; align-items: flex-start;">
        <h3 class="gradient-text" style="font-size: 24px; margin: 0;">🧠 UniComm</h3>
        <div class="cosmic-sphere" style="width: 40px; height: 40px;"></div>
      </div>
      <p style="font-style: italic; margin: 10px 0 20px;"><i>Universal accessibility communication platform</i></p>
      
      <div style="display: flex; flex-wrap: wrap; gap: 8px; margin: 15px 0;">
        <span class="tech-badge">React</span>
        <span class="tech-badge">Next.js</span>
        <span class="tech-badge">MediaPipe</span>
      </div>
      
      <ul style="padding-left: 20px; line-height: 1.6;">
        <li>Real-time sign language translation</li>
        <li>8+ sign language dialects supported</li>
        <li>Award-winning accessibility solution</li>
      </ul>
      
      <!-- ANIMATED PROGRESS BAR -->
      <div class="progress-container">
        <div class="progress-bar" style="width: 91%;"></div>
      </div>
      <p align="right" style="margin: 5px 0 0;"><b>91% Complete</b></p>
    </div>
  </div>
  
  <!-- TECH COSMOS WITH 3D ANIMATION -->
  <h2 align="center" class="gradient-text" style="font-size: 32px; margin: 40px 0 20px;">🌠 Tech Cosmos</h2>
  <div align="center" style="margin-bottom: 30px;">
    <img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/aqua.png" alt="aqua" width="100%">
  </div>
  
  <!-- ANIMATED TECH STACK WITH HOVER EFFECTS -->
  <div class="glass-card cosmic-border" style="margin-bottom: 30px;">
    <div align="center">
      <div class="float">
        <!-- 3D Tech Galaxy -->
        <div style="position: relative; padding: 20px;">
          <!-- Background glow effect -->
          <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 80%; height: 80%; background: radial-gradient(circle, rgba(233, 64, 87, 0.1) 0%, rgba(138, 35, 135, 0.1) 50%, transparent 100%); filter: blur(30px); z-index: -1;"></div>
          
          <img src="https://skillicons.dev/icons?i=python,tensorflow,pytorch,react,nextjs,typescript,fastapi,docker,aws,gcp,kubernetes,opencv,solidity,graphql,mongodb,postgresql&perline=8" class="hover-lift" />
        </div>
      </div>
      
      <img src="https://i.imgur.com/dBaSKWF.gif" height="20" width="100%" style="margin: 30px 0;">
      
      <!-- Interactive skills radar -->
      <div class="card-3d">
        <img src="https://cr-skills-chart-widget.azurewebsites.net/api/api?username=amruthjakku&skills=AI,MachineLearning,NLP,ComputerVision,React,Web,Blockchain,Cloud&width=820&bg=transparent" width="80%" class="hover-lift" />
      </div>
      
      <!-- Skill proficiency bars with animation -->
      <div style="max-width: 700px; margin: 40px auto 0; text-align: left;">
        <h3 class="gradient-text" style="text-align: center; margin-bottom: 25px;">Core Expertise</h3>
        
        <div class="tech-exp">
          <div class="tech-name">
            <span>AI & Machine Learning</span>
            <span>95%</span>
          </div>
          <div class="progress-container">
            <div class="progress-bar" style="width: 95%;"></div>
          </div>
        </div>
        
        <div class="tech-exp">
          <div class="tech-name">
            <span>Computer Vision</span>
            <span>90%</span>
          </div>
          <div class="progress-container">
            <div class="progress-bar" style="width: 90%;"></div>
          </div>
        </div>
        
        <div class="tech-exp">
          <div class="tech-name">
            <span>Natural Language Processing</span>
            <span>88%</span>
          </div>
          <div class="progress-container">
            <div class="progress-bar" style="width: 88%;"></div>
          </div>
        </div>
        
        <div class="tech-exp">
          <div class="tech-name">
            <span>Full-Stack Development</span>
            <span>85%</span>
          </div>
          <div class="progress-container">
            <div class="progress-bar" style="width: 85%;"></div>
          </div>
        </div>
        
        <div class="tech-exp">
          <div class="tech-name">
            <span>Cloud Architecture</span>
            <span>82%</span>
          </div>
          <div class="progress-container">
            <div class="progress-bar" style="width: 82%;"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
  
  <!-- ACHIEVEMENTS WITH 3D CARDS -->
  <h2 align="center" class="gradient-text" style="font-size: 32px; margin: 40px 0 20px;">🏆 Cosmic Achievements</h2>
  <div align="center" style="margin-bottom: 30px;">
    <img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/colored.png" alt="colored" width="100%">
  </div>
  
  <!-- ACHIEVEMENT CARDS WITH 3D EFFECTS -->
  <div class="grid-3">
    <div class="glass-card card-3d" style="background: linear-gradient(135deg, rgba(138, 35, 135, 0.2), rgba(233, 64, 87, 0.2), rgba(242, 113, 33, 0.2)); border-radius: 16px; padding: 25px; border: 1px solid rgba(255, 255, 255, 0.1);">
      <div align="center">
        <div class="cosmic-sphere" style="width: 60px; height: 60px; margin-bottom: 15px;"></div>
        <h3 class="gradient-text" style="font-size: 22px; margin-bottom: 10px;">Hackathon Champion</h3>
        <p style="line-height: 1.6;">Built complete AI solutions in under 48 hours - recognized by judges for technical innovation.</p>
      </div>
    </div>
    
    <div class="glass-card card-3d" style="background: linear-gradient(135deg, rgba(138, 35, 135, 0.2), rgba(233, 64, 87, 0.2), rgba(242, 113, 33, 0.2)); border-radius: 16px; padding: 25px; border: 1px solid rgba(255, 255, 255, 0.1);">
      <div align="center">
        <div class="cosmic-sphere" style="width: 60px; height: 60px; margin-bottom: 15px;"></div>
        <h3 class="gradient-text" style="font-size: 22px; margin-bottom: 10px;">Innovation Fellow</h3>
        <p style="line-height: 1.6;">Selected for prestigious T-Hub AI Innovation Program from 2,000+ applicants nationwide.</p>
      </div>
    </div>
    
    <div class="glass-card card-3d" style="background: linear-gradient(135deg, rgba(138, 35, 135, 0.2), rgba(233, 64, 87, 0.2), rgba(242, 113, 33, 0.2)); border-radius: 16px; padding: 25px; border: 1px solid rgba(255, 255, 255, 0.1);">
      <div align="center">
        <div class="cosmic-sphere" style="width: 60px; height: 60px; margin-bottom: 15px;"></div>
        <h3 class="gradient-text" style="font-size: 22px; margin-bottom: 10px;">Featured Speaker</h3>
        <p style="line-height: 1.6;">AI Ethics & Innovation Summit - presented to 500+ industry professionals on responsible AI.</p>
      </div>
    </div>
  </div>
  
  <!-- GITHUB STATS WITH ANIMATED LOADING -->
  <h2 align="center" class="gradient-text" style="font-size: 32px; margin: 40px 0 20px;">⭐ GitHub Constellation</h2>
  <div align="center" style="margin-bottom: 30px;">
    <img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/fire.png" alt="fire" width="100%">
  </div>
  
  <div class="glass-card cosmic-border" style="margin-bottom: 30px;">
    <div align="center">
      <!-- GitHub activity graph with hover effects -->
      <div class="card-3d" style="margin-bottom: 25px;">
        <img src="https://github-readme-activity-graph.vercel.app/graph?username=amruthjakku&bg_color=0d1117&color=e05397&line=e05397&point=ffffff&area=true&hide_border=true" width="90%" alt="activity graph" class="hover-lift">
      </div>
      
      <!-- Stats cards with animated loading -->
      <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; margin-bottom: 25px;">
        <div class="glass-card card-3d" style="padding: 15px; min-width: 280px;">
          <img height="180em" src="https://github-readme-stats.vercel.app/api?username=amruthjakku&show_icons=true&theme=radical&include_all_commits=true&count_private=true&bg_color=0D1117&text_color=ffffff&icon_color=e05397&title_color=e05397" class="hover-lift"/>
          <div class="stat-bar" style="margin-top: 10px; animation-delay: 0.5s;"></div>
        </div>
        
        <div class="glass-card card-3d" style="padding: 15px; min-width: 280px;">
          <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=amruthjakku&layout=compact&langs_count=7&theme=radical&bg_color=0D1117&text_color=ffffff&icon_color=e05397&title_color=e05397" class="hover-lift"/>
          <div class="stat-bar" style="margin-top: 10px; animation-delay: 1s;"></div>
        </div>
      </div>
      
      <!-- Streak stats with glowing effect -->
      <div class="glass-card card-3d" style="padding: 15px; max-width: 600px; margin: 0 auto;">
        <img src="https://github-readme-streak-stats.herokuapp.com/?user=amruthjakku&theme=black-ice&hide_border=true&stroke=0000&background=0D1117&ring=e05397&fire=e05397&currStreakLabel=e05397" alt="streak stats" width="100%" class="hover-lift"/>
        <div class="stat-bar" style="margin-top: 10px; animation-delay: 1.5s;"></div>
      </div>
    </div>
  </div>
  
  <!-- LEARNING ORBIT WITH INTERACTIVE MIND MAP -->
  <h2 align="center" class="gradient-text" style="font-size: 32px; margin: 40px 0 20px;">🔭 Learning Orbit</h2>
  <div align="center" style="margin-bottom: 30px;">
    <img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/dark.png" alt="dark" width="100%">
  </div>
  
  <!-- INTERACTIVE ORBITAL LEARNING DIAGRAM -->
  <div class="glass-card cosmic-border" style="margin-bottom: 30px; padding: 30px;">
    <div style="position: relative; width: 100%; height: 400px; overflow: hidden;">
      <!-- Central core -->
      <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 100px; height: 100px; border-radius: 50%; background: linear-gradient(135deg, #8A2387, #E94057, #F27121); box-shadow: 0 0 30px rgba(233, 64, 87, 0.5); display: flex; justify-content: center; align-items: center; z-index: 10;">
        <span style="color: white; font-weight: bold; font-size: 18px; text-shadow: 0 0 5px rgba(0, 0, 0, 0.5);">AI Mastery</span>
      </div>
      
      <!-- Orbit paths -->
      <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 300px; height: 300px; border-radius: 50%; border: 1px dashed rgba(255, 255, 255, 0.2); animation: rotate 30s linear infinite;"></div>
      <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 500px; height: 500px; border-radius: 50%; border: 1px dashed rgba(255, 255, 255, 0.2); animation: rotate 40s linear infinite reverse;"></div>
      <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 700px; height: 200px; border-radius: 50%; border: 1px dashed rgba(255, 255, 255, 0.2); animation: rotate 50s linear infinite;"></div>
      
      <!-- Orbit 1 nodes -->
      <div class="glass-card hover-lift" style="position: absolute; top: 50%; left: 50%; transform: translate(-230px, -50%); padding: 15px; z-index: 5; width: 140px;">
        <h4 class="gradient-text" style="margin: 0 0 8px; font-size: 16px;">Advanced Models</h4>
        <ul style="padding-left: 15px; margin: 0; font-size: 14px;">
          <li>LLM Fine-tuning</li>
          <li>Reinforcement Learning</li>
          <li>Neural Architecture</li>
        </ul>
      </div>
      
      <div class="glass-card hover-lift" style="position: absolute; top: 50%; left: 50%; transform: translate(90px, -120px); padding: 15px; z-index: 5; width: 140px;">
        <h4 class="gradient-text" style="margin: 0 0 8px; font-size: 16px;">AI Ethics</h4>
        <ul style="padding-left: 15px; margin: 0; font-size: 14px;">
          <li>Alignment & Safety</li>
          <li>Bias Mitigation</li>
          <li>Explainable AI</li>
        </ul>
      </div>
      
      <div class="glass-card hover-lift" style="position: absolute; top: 50%; left: 50%; transform: translate(90px, 120px); padding: 15px; z-index: 5; width: 140px;">
        <h4 class="gradient-text" style="margin: 0 0 8px; font-size: 16px;">Systems Design</h4>
        <ul style="padding-left: 15px; margin: 0; font-size: 14px;">
          <li>MLOps & CI/CD</li>
          <li>Scalable Architecture</li>
          <li>Edge Deployment</li>
        </ul>
      </div>
      
      <div class="glass-card hover-lift" style="position: absolute; top: 25%; left: 50%; transform: translateX(-50%); padding: 15px; z-index: 5; width: 140px;">
        <h4 class="gradient-text" style="margin: 0 0 8px; font-size: 16px;">Multimodal AI</h4>
        <ul style="padding-left: 15px; margin: 0; font-size: 14px;">
          <li>Vision-Language</li>
          <li>Audio Processing</li>
          <li>Cross-modal Transfer</li>
        </ul>
      </div>
      
      <!-- Floating particles -->
      <div class="cosmic-sphere" style="position: absolute; top: 30%; left: 35%; width: 8px; height: 8px; animation: float 4s ease-in-out infinite;"></div>
      <div class="cosmic-sphere" style="position: absolute; top: 70%; left: 65%; width: 12px; height: 12px; animation: float 6s ease-in-out infinite;"></div>
      <div class="cosmic-sphere" style="position: absolute; top: 20%; left: 70%; width: 10px; height: 10px; animation: float 5s ease-in-out infinite;"></div>
      <div class="cosmic-sphere" style="position: absolute; top: 60%; left: 30%; width: 15px; height: 15px; animation: float 7s ease-in-out infinite;"></div>
    </div>
  </div>
  
  <!-- PUBLICATIONS WITH HOVER EFFECTS -->
  <h2 align="center" class="gradient-text" style="font-size: 32px; margin: 40px 0 20px;">📚 Research Nebula</h2>
  <div align="center" style="margin-bottom: 30px;">
    <img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="rainbow" width="100%">
  </div>
  
  <div class="grid-1">
    <!-- Publication 1 -->
    <div class="glass-card hover-lift cosmic-border" style="margin-bottom: 20px; transition: all 0.3s ease;">
      <div style="display: flex; align-items: center; gap: 20px;">
        <div class="cosmic-sphere pulse" style="min-width: 50px; height: 50px; border-radius: 12px;"></div>
        <div>
          <h3 class="gradient-text" style="font-size: 20px; margin: 0 0 8px;">Ethical Frameworks for AI in Law Enforcement</h3>
          <p style="color: #E94057; margin: 0 0 10px; font-size: 14px;">International Journal of AI Ethics | 2024</p>
          <p style="margin: 0; line-height: 1.6;">Exploring the balance between security and privacy in AI-powered crime detection systems.</p>
        </div>
      </div>
    </div>
    
    <!-- Publication 2 -->
    <div class="glass-card hover-lift cosmic-border" style="margin-bottom: 20px; transition: all 0.3s ease;">
      <div style="display: flex; align-items: center; gap: 20px;">
        <div class="cosmic-sphere pulse" style="min-width: 50px; height: 50px; border-radius: 12px;"></div>
        <div>
          <h3 class="gradient-text" style="font-size: 20px; margin: 0 0 8px;">Breaking Communication Barriers: AI for Accessibility</h3>
          <p style="color: #E94057; margin: 0 0 10px; font-size: 14px;">ACM Conference on Accessible Technologies | 2024</p>
          <p style="margin: 0; line-height: 1.6;">Novel approaches to accessibility technology for hearing impaired communities.</p>
        </div>
      </div>
    </div>
    
    <!-- Publication 3 -->
    <div class="glass-card hover-lift cosmic-border" style="margin-bottom: 20px; transition: all 0.3s ease;">
      <div style="display: flex; align-items: center; gap: 20px;">
        <div class="cosmic-sphere pulse" style="min-width: 50px; height: 50px; border-radius: 12px;"></div>
        <div>
          <h3 class="gradient-text" style="font-size: 20px; margin: 0 0 8px;">Blockchain and AI: A Framework for Evidence Integrity</h3>
          <p style="color: #E94057; margin: 0 0 10px; font-size: 14px;">IEEE Security & Privacy | 2023</p>
          <p style="margin: 0; line-height: 1.6;">Implementing tamper-proof systems for sensitive data in law enforcement.</p>
        </div>
      </div>
    </div>
  </div>
  
  <!-- CONTACT SECTION WITH ANIMATION -->
  <h2 align="center" class="gradient-text" style="font-size: 32px; margin: 40px 0 20px;">🌌 Interstellar Contact</h2>
  <div align="center" style="margin-bottom: 30px;">
    <img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/solar.png" alt="solar" width="100%">
  </div>
  
  <div class="glass-card cosmic-border" style="text-align: center; padding: 40px; margin-bottom: 30px;">
    <div class="float">
      <!-- Interactive contact animation -->
      <div style="position: relative; width: 200px; height: 200px; margin: 0 auto 30px;">
        <!-- Orbits -->
        <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 180px; height: 180px; border-radius: 50%; border: 1px dashed rgba(255, 255, 255, 0.2); animation: rotate 15s linear infinite;"></div>
        <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 120px; height: 120px; border-radius: 50%; border: 1px dashed rgba(255, 255, 255, 0.2); animation: rotate 10s linear infinite reverse;"></div>
        
        <!-- Central element -->
        <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); display: flex; justify-content: center; align-items: center;">
          <div class="cosmic-sphere" style="width: 60px; height: 60px;"></div>
        </div>
        
        <!-- Orbiting elements with icons -->
        <div style="position: absolute; top: 20px; left: 50%; transform: translateX(-50%); background: rgba(255, 255, 255, 0.1); width: 40px; height: 40px; border-radius: 50%; display: flex; justify-content: center; align-items: center;">
          <span style="font-size: 20px;">✉️</span>
        </div>
        <div style="position: absolute; bottom: 20px; left: 50%; transform: translateX(-50%); background: rgba(255, 255, 255, 0.1); width: 40px; height: 40px; border-radius: 50%; display: flex; justify-content: center; align-items: center;">
          <span style="font-size: 20px;">🌐</span>
        </div>
        <div style="position: absolute; left: 20px; top: 50%; transform: translateY(-50%); background: rgba(255, 255, 255, 0.1); width: 40px; height: 40px; border-radius: 50%; display: flex; justify-content: center; align-items: center;">
          <span style="font-size: 20px;">💬</span>
        </div>
        <div style="position: absolute; right: 20px; top: 50%; transform: translateY(-50%); background: rgba(255, 255, 255, 0.1); width: 40px; height: 40px; border-radius: 50%; display: flex; justify-content: center; align-items: center;">
          <span style="font-size: 20px;">🔗</span>
        </div>
      </div>
    </div>
    
    <p style="font-size: 18px; line-height: 1.6; max-width: 700px; margin: 0 auto 20px;">I'm always open to collaborations on innovative AI projects, research opportunities, hackathons, and building technology that matters.</p>
    
    <a href="mailto:amruthjakku@gmail.com" class="hover-lift" style="display: inline-block; margin-bottom: 30px;">
      <div class="cosmic-border" style="padding: 2px;">
        <div style="background: rgba(13, 17, 23, 0.8); padding: 8px 25px; border-radius: 14px;">
          <span class="gradient-text" style="font-size: 18px; font-weight: bold;">Contact Me</span>
        </div>
      </div>
    </a>
    
    <p style="font-style: italic; margin-bottom: 20px;"><i>"The best way to predict the future is to create it."</i></p>
    
    <div class="card-3d">
      <img src="https://count.getloli.com/get/@:amruthjakku?theme=rule34" alt="visitor counter" />
    </div>
  </div>
  
  <!-- ANIMATED FOOTER -->
  <div align="center">
    <img src="https://capsule-render.vercel.app/api?type=waving&height=150&section=footer&text=&fontAlign=80&fontAlignY=40&color=gradient&customColorList=24" width="100%">
  </div>
</div>

<!-- 3D Effect with Parallax -->
<script>
  document.addEventListener('DOMContentLoaded', function() {
    // Add parallax effect to elements with data-depth
    document.addEventListener('mousemove', function(e) {
      const parallaxElements = document.querySelectorAll('.parallax');
      const mouseX = (e.clientX / window.innerWidth) - 0.5;
      const mouseY = (e.clientY / window.innerHeight) - 0.5;
      
      parallaxElements.forEach(el => {
        const depth = el.getAttribute('data-depth') || 0.2;
        const moveX = mouseX * depth * 40;
        const moveY = mouseY * depth * 40;
        el.style.transform = `translate3d(${moveX}px, ${moveY}px, 0)`;
      });
    });
    
    // Generate stars for star field
    const starField = document.querySelector('.star-field');
    for (let i = 0; i < 100; i++) {
      const star = document.createElement('div');
      star.classList.add('star');
      star.style.top = `${Math.random() * 100}%`;
      star.style.left = `${Math.random() * 100}%`;
      star.style.animationDelay = `${Math.random() * 5}s`;
      star.style.width = `${Math.random() * 2 + 1}px`;
      star.style.height = star.style.width;
      starField.appendChild(star);
    }
    
    // Animate progress bars on scroll
    const progressBars = document.querySelectorAll('.progress-bar');
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.style.width = entry.target.parentElement.nextElementSibling.textContent;
        }
      });
    }, { threshold: 0.5 });
    
    progressBars.forEach(bar => {
      observer.observe(bar);
    });
  });
</script>
