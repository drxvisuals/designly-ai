<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AI Tool Landing Page</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
<style>
  /* ===== Global Styles ===== */
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Inter', sans-serif;
  }
  body {
    background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
    color: #fff;
    overflow-x: hidden;
  }
  a {
    text-decoration: none;
    color: inherit;
  }

  /* ===== Container ===== */
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
  }

  /* ===== Hero Section ===== */
  .hero {
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute;
    width: 120%;
    height: 120%;
    top: -10%;
    left: -10%;
    background: radial-gradient(circle, rgba(255,255,255,0.05), transparent 70%);
    animation: rotate 20s linear infinite;
  }
  @keyframes rotate {
    0% { transform: rotate(0deg);}
    100% { transform: rotate(360deg);}
  }

  .hero h1 {
    font-size: 3rem;
    margin-bottom: 20px;
    text-shadow: 0 0 20px rgba(255,255,255,0.3);
  }
  .hero p {
    font-size: 1.2rem;
    margin-bottom: 40px;
    color: #ccc;
  }
  .cta-btn {
    background: linear-gradient(135deg, #ff416c, #ff4b2b);
    padding: 15px 40px;
    border-radius: 50px;
    font-weight: 600;
    transition: all 0.3s ease;
    box-shadow: 0 8px 20px rgba(255,75,43,0.4);
  }
  .cta-btn:hover {
    transform: scale(1.05);
    box-shadow: 0 12px 30px rgba(255,75,43,0.6);
  }

  /* ===== Features Section ===== */
  .features {
    padding: 100px 0;
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    gap: 30px;
  }
  .feature-card {
    backdrop-filter: blur(10px);
    background: rgba(255,255,255,0.05);
    border-radius: 20px;
    padding: 40px;
    width: 280px;
    text-align: center;
    transition: all 0.3s ease;
    cursor: pointer;
  }
  .feature-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 35px rgba(255,255,255,0.2);
  }
  .feature-card img {
    width: 80px;
    margin-bottom: 20px;
  }
  .feature-card h3 {
    margin-bottom: 10px;
    font-size: 1.5rem;
  }
  .feature-card p {
    color: #ccc;
    font-size: 0.95rem;
  }

  /* ===== Testimonials Section ===== */
  .testimonials {
    background: rgba(255,255,255,0.05);
    padding: 80px 0;
    text-align: center;
  }
  .testimonial-card {
    display: inline-block;
    background: rgba(0,0,0,0.4);
    backdrop-filter: blur(10px);
    padding: 30px;
    margin: 20px;
    border-radius: 20px;
    max-width: 300px;
    transition: all 0.3s ease;
  }
  .testimonial-card:hover {
    transform: translateY(-5px);
  }
  .testimonial-card p {
    font-style: italic;
    margin-bottom: 15px;
  }
  .testimonial-card h4 {
    color: #ff416c;
  }

  /* ===== Footer ===== */
  footer {
    text-align: center;
    padding: 40px 20px;
    background: rgba(0,0,0,0.7);
    color: #aaa;
    font-size: 0.9rem;
  }

  /* ===== Scroll Animations ===== */
  .fade-in {
    opacity: 0;
    transform: translateY(30px);
    animation: fadeInUp 1s forwards;
  }
  @keyframes fadeInUp {
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>
</head>
<body>

  <!-- Hero Section -->
  <section class="hero">
    <h1 class="fade-in" style="animation-delay:0.3s">Revolutionize Your Work with AI</h1>
    <p class="fade-in" style="animation-delay:0.6s">Create, design, and innovate faster than ever with our AI-powered tool.</p>
    <a href="#features" class="cta-btn fade-in" style="animation-delay:0.9s">Try It Now</a>
  </section>

  <!-- Features Section -->
  <section id="features" class="features">
    <div class="feature-card fade-in" style="animation-delay:0.3s">
      <img src="https://img.icons8.com/ios-filled/100/ffffff/robot.png" alt="AI Icon">
      <h3>AI Generation</h3>
      <p>Instantly generate creative content with our powerful AI algorithms.</p>
    </div>
    <div class="feature-card fade-in" style="animation-delay:0.5s">
      <img src="https://img.icons8.com/ios-filled/100/ffffff/settings.png" alt="Custom Icon">
      <h3>Customizable</h3>
      <p>Adjust parameters and styles to make the AI output truly yours.</p>
    </div>
    <div class="feature-card fade-in" style="animation-delay:0.7s">
      <img src="https://img.icons8.com/ios-filled/100/ffffff/speed.png" alt="Speed Icon">
      <h3>Fast & Efficient</h3>
      <p>Get results in seconds and boost your productivity exponentially.</p>
    </div>
  </section>

  <!-- Testimonials Section -->
  <section class="testimonials">
    <h2 class="fade-in" style="animation-delay:0.3s">What Users Say</h2>
    <div class="testimonial-card fade-in" style="animation-delay:0.5s">
      <p>"This AI tool transformed my workflow! Absolutely mind-blowing."</p>
      <h4>- Alex J.</h4>
    </div>
    <div class="testimonial-card fade-in" style="animation-delay:0.7s">
      <p>"Highly recommend! The interface is smooth and intuitive."</p>
      <h4>- Maria K.</h4>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    &copy; 2025 AI Tool. All Rights Reserved.
  </footer>

  <!-- JS for fade-in on scroll -->
  <script>
    const faders = document.querySelectorAll('.fade-in');
    const appearOptions = {
      threshold: 0.3
    };
    const appearOnScroll = new IntersectionObserver(function(entries, observer){
      entries.forEach(entry => {
        if (!entry.isIntersecting) return;
        entry.target.style.animationPlayState = 'running';
        observer.unobserve(entry.target);
      });
    }, appearOptions);
    faders.forEach(fader => {
      fader.style.animationPlayState = 'paused';
      appearOnScroll.observe(fader);
    });
  </script>

</body>
</html>