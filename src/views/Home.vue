<template>
  <div class="home">
    <!-- Hero Section -->
    <section class="hero">
      <div class="container">
        <div class="hero-content">
          <h1>Parallel Balanced <span>Wheel-Leg Robot</span></h1>
          <p>
            A research project focused on enhancing the adaptability and movement efficiency of wheel-legged robots 
            in complex terrain using Deep Reinforcement Learning.
          </p>
          <div class="hero-buttons">
            <router-link to="/timeline" class="btn">View Timeline</router-link>
            <router-link to="/statistics" class="btn btn-outline">See Statistics</router-link>
          </div>
        </div>
        <div class="hero-image">
          <img src="@/assets/hero-image.svg" alt="Wheel-Leg Robot" />
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section class="section features-section">
      <div class="container">
        <div class="section-title">
          <h2>Project Objectives</h2>
          <p>Our research aims to advance wheel-legged robots control to make them more efficient and reliable in real-world applications.</p>
        </div>

        <div class="features">
          <div class="feature-card">
            <div class="feature-icon">
              <i class="fas fa-cogs"></i>
            </div>
            <h3>Robot Design & Construction</h3>
            <p>Developing an innovative wheel-legged robot with a 5-link balanced wheel-leg structure to improve stability and agility.</p>
          </div>

          <div class="feature-card">
            <div class="feature-icon">
              <i class="fas fa-brain"></i>
            </div>
            <h3>Control System Development</h3>
            <p>Implementing a deep reinforcement learning based control system that enables autonomous locomotion strategy optimization.</p>
          </div>

          <div class="feature-card">
            <div class="feature-icon">
              <i class="fas fa-mountain"></i>
            </div>
            <h3>Terrain Adaptation</h3>
            <p>Enhancing the robot's ability to move through different environments while maintaining stable walking and avoiding obstacles.</p>
          </div>

          <div class="feature-card">
            <div class="feature-icon">
              <i class="fas fa-microchip"></i>
            </div>
            <h3>Edge Computing Deployment</h3>
            <p>Enabling edge computing for control systems to reduce latency and improve real-time responsiveness of the robot.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Overview Section -->
    <section class="section overview-section">
      <div class="container">
        <div class="section-title">
          <h2>Project Overview</h2>
          <p>Current progress and achievements in our robotic research as of June 1, 2025.</p>
        </div>

        <div class="overview-content">
          <div class="overview-card">
            <h3>Current Status</h3>
            <div class="status-indicator">
              <div class="progress-bar">
                <div class="progress" style="width: 100%;"></div>
              </div>
              <p><span>100%</span> Complete</p>
            </div>
            <ul class="status-details">
              <li><i class="fas fa-check-circle"></i> Mechanical Structures: <span>Completed</span></li>
              <li><i class="fas fa-check-circle"></i> Electrical Control: <span>Completed</span></li>
              <li><i class="fas fa-check-circle"></i> Simulation Environment: <span>Completed</span></li>
              <li><i class="fas fa-check-circle"></i> Hardware Refinement: <span>Completed</span></li>
              <li><i class="fas fa-check-circle"></i> Model Fine-tuning: <span>Completed</span></li>
              <li><i class="fas fa-check-circle"></i> Final Testing: <span>Completed</span></li>
            </ul>
          </div>

          <div class="overview-card">
            <h3>Key Achievements</h3>
            <ul class="achievements-list">
              <li>
                <div class="achievement-icon"><i class="fas fa-cogs"></i></div>
                <div class="achievement-content">
                  <h4>Hardware System Refinement</h4>
                  <p>Enhanced SolidWorks models with NUC and voltage regulator, completed robot assembly with comprehensive wiring</p>
                </div>
              </li>
              <li>
                <div class="achievement-icon"><i class="fas fa-wifi"></i></div>
                <div class="achievement-content">
                  <h4>Wireless Control GUI</h4>
                  <p>Developed GUI for wireless debugging and control with cable soldering and system integration</p>
                </div>
              </li>
              <li>
                <div class="achievement-icon"><i class="fas fa-brain"></i></div>
                <div class="achievement-content">
                  <h4>Isaac Lab Migration</h4>
                  <p>Upgraded from Isaac Gym to Isaac Lab for enhanced simulation performance and expanded task support</p>
                </div>
              </li>
              <li>
                <div class="achievement-icon"><i class="fas fa-chart-line"></i></div>
                <div class="achievement-content">
                  <h4>Model Fine-tuning Success</h4>
                  <p>Improved robot stability from unstable leg positioning to normal operation through parameter optimization</p>
                </div>
              </li>
              <li>
                <div class="achievement-icon"><i class="fas fa-flag-checkered"></i></div>
                <div class="achievement-content">
                  <h4>Real-world Deployment Completed</h4>
                  <p>Neural network deployed and tested successfully in real-world environments</p>
                </div>
              </li>
              <li>
                <div class="achievement-icon"><i class="fas fa-clipboard-check"></i></div>
                <div class="achievement-content">
                  <h4>Final Report Submitted</h4>
                  <p>Final research report and presentation submitted on July 15, 2025</p>
                </div>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="section cta-section">
      <div class="container">
        <div class="cta-content">
          <h2>Ready to Explore More?</h2>
          <p>Check out our detailed timeline and project statistics for a deeper understanding of our progress in developing the wheel-leg robot.</p>
          <div class="cta-buttons">
            <router-link to="/timeline" class="btn">View Timeline</router-link>
            <router-link to="/statistics" class="btn btn-outline">See Statistics</router-link>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'Home'
}
</script>

<style scoped>
/* Hero Section */
.hero {
  height: 100vh;
  background: linear-gradient(135deg, rgba(255, 255, 255, 0.9) 0%, rgba(255, 255, 255, 0.8) 100%);
  display: flex;
  align-items: center;
  position: relative;
  overflow: hidden;
}

.hero::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: url('@/assets/pattern.svg') repeat;
  opacity: 0.05;
  z-index: -1;
}

.hero .container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
  align-items: center;
}

.hero-content h1 {
  font-size: 3.5rem;
  font-weight: 700;
  margin-bottom: 1.5rem;
  line-height: 1.2;
}

.hero-content h1 span {
  color: var(--primary-color);
}

.hero-content p {
  font-size: 1.1rem;
  color: var(--secondary-color);
  margin-bottom: 2rem;
  max-width: 600px;
}

.hero-buttons {
  display: flex;
  gap: 1rem;
}

.hero-image img {
  width: 100%;
  max-width: 500px;
  animation: float 6s ease-in-out infinite;
}

@keyframes float {
  0% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-20px);
  }
  100% {
    transform: translateY(0px);
  }
}

/* Features Section */
.features-section {
  background-color: var(--light-color);
}

.features {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.feature-card {
  background-color: white;
  padding: 2rem;
  border-radius: var(--border-radius);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
  transition: var(--transition);
}

.feature-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
}

.feature-icon {
  font-size: 2.5rem;
  color: var(--primary-color);
  margin-bottom: 1.5rem;
}

.feature-card h3 {
  font-size: 1.5rem;
  margin-bottom: 1rem;
}

.feature-card p {
  color: var(--secondary-color);
}

/* Overview Section */
.overview-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.overview-card {
  background-color: white;
  padding: 2rem;
  border-radius: var(--border-radius);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
}

.overview-card h3 {
  font-size: 1.5rem;
  margin-bottom: 1.5rem;
  position: relative;
}

.overview-card h3::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: -10px;
  width: 50px;
  height: 3px;
  background-color: var(--primary-color);
}

.status-indicator {
  margin-bottom: 1.5rem;
}

.progress-bar {
  height: 10px;
  background-color: var(--border-color);
  border-radius: 5px;
  overflow: hidden;
  margin-bottom: 0.5rem;
}

.progress {
  height: 100%;
  background-color: var(--primary-color);
  border-radius: 5px;
}

.status-indicator p {
  text-align: right;
  font-size: 0.9rem;
  color: var(--secondary-color);
}

.status-indicator p span {
  font-weight: 700;
  color: var(--primary-color);
}

.status-details {
  list-style: none;
}

.status-details li {
  display: flex;
  align-items: center;
  margin-bottom: 1rem;
  color: var(--secondary-color);
}

.status-details li i {
  margin-right: 10px;
  color: var(--primary-color);
}

.status-details li span {
  margin-left: auto;
  font-weight: 500;
}

.achievements-list {
  list-style: none;
}

.achievements-list li {
  display: flex;
  margin-bottom: 1.5rem;
}

.achievement-icon {
  width: 50px;
  height: 50px;
  background-color: rgba(74, 108, 247, 0.1);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.2rem;
  color: var(--primary-color);
  margin-right: 1rem;
}

.achievement-content h4 {
  font-size: 1.1rem;
  margin-bottom: 0.3rem;
}

.achievement-content p {
  color: var(--secondary-color);
  font-size: 0.9rem;
}

/* CTA Section */
.cta-section {
  background: linear-gradient(135deg, var(--primary-color) 0%, #3a4fd7 100%);
  color: white;
  text-align: center;
}

.cta-content h2 {
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

.cta-content p {
  max-width: 600px;
  margin: 0 auto 2rem;
  opacity: 0.9;
}

.cta-buttons {
  display: flex;
  justify-content: center;
  gap: 1rem;
}

.cta-buttons .btn {
  background-color: white;
  color: var(--primary-color);
}

.cta-buttons .btn:hover {
  background-color: rgba(255, 255, 255, 0.9);
}

.cta-buttons .btn-outline {
  background-color: transparent;
  border: 2px solid white;
  color: white;
}

.cta-buttons .btn-outline:hover {
  background-color: white;
  color: var(--primary-color);
}

/* Responsive Styles */
@media (max-width: 992px) {
  .hero-content h1 {
    font-size: 3rem;
  }
}

@media (max-width: 768px) {
  .hero .container {
    grid-template-columns: 1fr;
    text-align: center;
  }

  .hero-content {
    order: 2;
  }

  .hero-image {
    order: 1;
  }

  .hero-content p {
    margin: 0 auto 2rem;
  }

  .hero-buttons {
    justify-content: center;
  }

  .hero-content h1 {
    font-size: 2.5rem;
  }
}

@media (max-width: 576px) {
  .hero-content h1 {
    font-size: 2rem;
  }

  .hero-buttons {
    flex-direction: column;
  }

  .cta-buttons {
    flex-direction: column;
    align-items: center;
  }
}
</style> 