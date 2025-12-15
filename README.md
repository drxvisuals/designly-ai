<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>AI Landing Page</title>

<style>
/* =====================
   THEME VARIABLES
===================== */
:root {
  --bg: #f6f8fc;
  --text: #0b0d17;
  --card: rgba(255,255,255,0.65);
  --border: rgba(255,255,255,0.4);
}

.dark {
  --bg: #0b0d17;
  --text: #ffffff;
  --card: rgba(20,20,30,0.65);
  --border: rgba(255,255,255,0.15);
}

/* =====================
   GLOBAL
===================== */
* {
  box-sizing: border-box;
  font-family: Inter, system-ui, sans-serif;
}

body {
  margin: 0;
  background: var(--bg);
  color: var(--text);
  transition: background 0.6s ease, color 0.6s ease;
  overflow-x: hidden;
}

/* =====================
   HERO
===================== */
.hero {
  min-height: 100vh;
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  padding: 5rem;
  gap: 3rem;
}

.hero-content h1 {
  font-size: 3.5rem;
  margin-bottom: 1rem;
}

.hero-content p {
  font-size: 1.2rem;
  opacity: 0.8;
  margin-bottom: 2.5rem;
}

/* =====================
   CTA BUTTON
===================== */
.cta {
  position: relative;
  padding: 1.2rem 3rem;
  font-size: 1.1rem;
  border-radius: 999px;
  border: none;
  cursor: pointer;
  color: white;
  background: linear-gradient(135deg, #3b82f6, #06b6d4);
  box-shadow: 0 0 35px rgba(59,130,246,0.7);
  overflow: hidden;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.cta:hover {
  transform: scale(1.1);
  box-shadow: 0 0 60px rgba(59,130,246,1);
}

.cta:active {
  transform: scale(0.95);
}

.cta .glow {
  position: absolute;
  inset: -50%;
  background: radial-gradient(circle, rgba(255,255,255,0.6), transparent 70%);
  animation: pulse 3s infinite;
}

@keyframes pulse {
  0%,100% { opacity: 0.4; }
  50% { opacity: 1; }
}

/* =====================
   SLIME BALL (3D FEEL)
===================== */
.slime-wrapper {
  position: relative;
  height: 300px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.slime {
  width: 180px;
  height: 180px;
  border-radius: 50%;
  background: radial-gradient(circle at 30% 30%, #7dd3fc, #2563eb);
  animation: bounce 3s ease-in-out infinite,
             hue 6s linear infinite;
  filter: blur(0.3px);
}

.shadow {
  position: absolute;
  bottom: 40px;
  width: 120px;
  height: 30px;
  background: rgba(0,0,0,0.25);
  filter: blur(18px);
  animation: shadow 3s ease-in-out infinite;
}

@keyframes bounce {
  0%,100% { transform: translateY(0) scale(1); }
  50% { transform: translateY(-120px) scale(1.08,0.92); }
}

@keyframes shadow {
  0%,100% { transform: scale(1); opacity: 0.3; }
  50% { transform: scale(0.6); opacity: 0.1; }
}

@keyframes hue {
  0% { filter: hue-rotate(0deg); }
  100% { filter: hue-rotate(360deg); }
}

/* =====================
   FEATURES (LIQUID GLASS)
===================== */
.features {
  padding: 5rem;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.glass-card {
  background: var(--card);
  backdrop-filter: blur(22px);
  border: 1px solid var(--border);
  border-radius: 24px;
  padding: 2rem;
  box-shadow: 0 25px 50px rgba(0,0,0,0.12);
  transition: transform 0.4s ease;
}

.glass-card:hover {
  transform: translateY(-12px);
}

/* =====================
   RESPONSIVE
===================== */
@media (max-width: 900px) {
  .hero {
    grid-template-columns: 1fr;
    text-align: center;
  }
}
</style>
</head>

<body>

<div class="page" id="page">

  <!-- HERO -->
  <section class="hero">
    <div class="hero-content">
      <h1>AI That Feels Alive</h1>
      <p>Design, generate, and innovate with a new kind of intelligence.</p>

      <button class="cta" id="toggleTheme">
        Get Started
        <span class="glow"></span>
      </button>
    </div>

    <!-- SLIME -->
    <div class="slime-wrapper">
      <div class="slime"></div>
      <div class="shadow"></div>
    </div>
  </section>

  <!-- FEATURES -->
  <section class="features">
    <div class="glass-card">
      <h3>Creative AI</h3>
      <p>Generate ideas, visuals and content instantly.</p>
    </div>
    <div class="glass-card">
      <h3>Liquid Interface</h3>
      <p>Glassmorphism UI with smooth motion.</p>
    </div>
    <div class="glass-card">
      <h3>Fast & Smart</h3>
      <p>Instant responses powered by AI.</p>
    </div>
  </section>

</div>

<script>
/* =====================
   THEME TOGGLE
===================== */
const button = document.getElementById("toggleTheme");
const page = document.getElementById("page");

button.addEventListener("click", () => {
  page.classList.toggle("dark");
});
</script>

</body>
</html>