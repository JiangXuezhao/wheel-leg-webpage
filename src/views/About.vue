<template>
  <div class="about-page">
    <!-- Page Header -->
    <section class="page-header">
      <div class="container">
        <h1>About the Project</h1>
        <p>Learn more about our Wheel-Leg Robot project, team and methodology</p>
      </div>
    </section>

    <!-- Project Overview Section -->
    <section class="section overview-section">
      <div class="container">
        <div class="section-title">
          <h2>Project Overview</h2>
          <p>A comprehensive introduction to our research on wheel-legged robots</p>
        </div>

        <div class="overview-content">
          <div class="overview-image">
            <img src="@/assets/about-project.svg" alt="Project Overview" />
          </div>
          <div class="overview-text">
            <h3>What We're Building</h3>
            <p>
              This project aims to improve the adaptability and movement efficiency of wheel-legged robots in complex terrain. 
              We're developing an innovative wheel-legged robot with a 5-link balanced wheel-leg structure to enhance stability 
              and agility, allowing the robot to effectively respond to different environmental challenges.
            </p>
            <h3>Our Vision</h3>
            <p>
              Our vision is to advance the control of wheel-legged robots to make them more efficient and reliable in real-world 
              applications, especially in complex and dynamic environments. By integrating deep reinforcement learning techniques, 
              we aim to create robots that can autonomously learn and optimize their locomotion strategies.
            </p>
            <h3>Key Objectives</h3>
            <ul class="objectives-list">
              <li><i class="fas fa-check-circle"></i> Design and build an innovative wheel-legged robot with a 5-link balanced structure</li>
              <li><i class="fas fa-check-circle"></i> Develop a deep reinforcement learning based control system</li>
              <li><i class="fas fa-check-circle"></i> Enhance terrain adaptation capabilities in diverse environments</li>
              <li><i class="fas fa-check-circle"></i> Deploy control systems in edge computing environments</li>
              <li><i class="fas fa-check-circle"></i> Conduct comprehensive experimentation and performance evaluation</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- Team Section -->
    <section class="section team-section">
      <div class="container">
        <div class="section-title">
          <h2>Our Team</h2>
          <p>Meet the researchers behind this project</p>
        </div>

        <div class="team-cards">
          <div class="team-card">
            <div class="team-photo">
              <img src="@/assets/team-1.svg" alt="Team Member" />
            </div>
            <div class="team-info">
              <h3>Wu Jiatong</h3>
              <p class="team-role">Project Leader</p>
              <p class="team-bio">
                Focusing on mechanical design and simulation of the wheel-leg robot structure.
              </p>
            </div>
          </div>

          <div class="team-card">
            <div class="team-photo">
              <img src="@/assets/team-2.svg" alt="Team Member" />
            </div>
            <div class="team-info">
              <h3>Wu Teng</h3>
              <p class="team-role">Team Member</p>
              <p class="team-bio">
                Contributing expertise in control systems and reinforcement learning algorithms to optimize robot movement.
              </p>
            </div>
          </div>

          <div class="team-card">
            <div class="team-photo">
              <img src="@/assets/team-3.svg" alt="Team Member" />
            </div>
            <div class="team-info">
              <h3>Jiang Xuezhao</h3>
              <p class="team-role">Team Member</p>
              <p class="team-bio">
                Contributing expertise in webpage development and deep reinforcement learning algorithms to optimize robot movement.
              </p>
            </div>
          </div>

          <div class="team-card">
            <div class="team-photo">
              <img src="@/assets/team-4.svg" alt="Team Member" />
            </div>
            <div class="team-info">
              <h3>Wen Hao</h3>
              <p class="team-role">Team Member</p>
              <p class="team-bio">
                Specialized in hardware integration and sensor data processing for the wheel-leg robot.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Methodology Section -->
    <section class="section methodology-section">
      <div class="container">
        <div class="section-title">
          <h2>Our Methodology</h2>
          <p>How we approach the development and research of wheel-legged robots</p>
        </div>

        <div class="methodology-content">
          <div class="methodology-item">
            <div class="methodology-icon">
              <i class="fas fa-drafting-compass"></i>
            </div>
            <div class="methodology-info">
              <h3>Robot Design & Construction</h3>
              <p>
                We design a five-link balanced wheel leg structure, considering stability and maneuverability on different terrains. 
                The modeling is performed using SolidWorks, with thorough verification of the structure's strength and stiffness. 
                We carefully select and integrate hardware components to ensure optimal performance.
              </p>
            </div>
          </div>

          <div class="methodology-item">
            <div class="methodology-icon">
              <i class="fas fa-cogs"></i>
            </div>
            <div class="methodology-info">
              <h3>Control System Development</h3>
              <p>
                Our control system is built on the ROS platform, utilizing its functional libraries and tools. We develop 
                sensor data processing modules to acquire environmental information in real-time. The control algorithm 
                includes both a model-based baseline strategy and optimization through deep reinforcement learning.
              </p>
            </div>
          </div>

          <div class="methodology-item">
            <div class="methodology-icon">
              <i class="fas fa-brain"></i>
            </div>
            <div class="methodology-info">
              <h3>Deep Reinforcement Learning</h3>
              <p>
                We construct simulation environments using platforms like Wheel-Legged-Gym to create diverse training scenarios. 
                Our DRL approach includes carefully designed reward functions and selection of suitable algorithms such as 
                DQN and PPO. We implement domain randomization techniques to enhance the generalization of training models.
              </p>
            </div>
          </div>

          <div class="methodology-item">
            <div class="methodology-icon">
              <i class="fas fa-vial"></i>
            </div>
            <div class="methodology-info">
              <h3>Experimentation & Evaluation</h3>
              <p>
                We design comprehensive experiments to evaluate robot performance across different terrains, measuring metrics like 
                speed, stability, and energy consumption. Results are analyzed using both quantitative and qualitative methods 
                to assess the effectiveness of our deep reinforcement learning algorithms.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Technologies Section -->
    <section class="section technologies-section">
      <div class="container">
        <div class="section-title">
          <h2>Technologies We Use</h2>
          <p>The technical stack that powers our wheel-leg robot</p>
        </div>

        <div class="tech-container">
          <div class="tech-category">
            <h3>Simulation & Training</h3>
            <div class="tech-list">
              <div class="tech-item">
                <div class="tech-icon">
                  <i class="fas fa-cube"></i>
                </div>
                <span>Wheel-Legged-Gym</span>
              </div>
              <div class="tech-item">
                <div class="tech-icon">
                  <i class="fas fa-robot"></i>
                </div>
                <span>legged_gym</span>
              </div>
              <div class="tech-item">
                <div class="tech-icon">
                  <i class="fas fa-brain"></i>
                </div>
                <span>rsl_rl</span>
              </div>
              <div class="tech-item">
                <div class="tech-icon">
                  <i class="fab fa-python"></i>
                </div>
                <span>Python</span>
              </div>
            </div>
          </div>

          <div class="tech-category">
            <h3>Control System</h3>
            <div class="tech-list">
              <div class="tech-item">
                <div class="tech-icon">
                  <i class="fas fa-cog"></i>
                </div>
                <span>ROS</span>
              </div>
              <div class="tech-item">
                <div class="tech-icon">
                  <i class="fab fa-linux"></i>
                </div>
                <span>Linux</span>
              </div>
              <div class="tech-item">
                <div class="tech-icon">
                  <i class="fas fa-microchip"></i>
                </div>
                <span>Edge Computing</span>
              </div>
              <div class="tech-item">
                <div class="tech-icon">
                  <i class="fas fa-code"></i>
                </div>
                <span>C++</span>
              </div>
            </div>
          </div>

          <div class="tech-category">
            <h3>Design & Modeling</h3>
            <div class="tech-list">
              <div class="tech-item">
                <div class="tech-icon">
                  <i class="fas fa-drafting-compass"></i>
                </div>
                <span>SolidWorks</span>
              </div>
              <div class="tech-item">
                <div class="tech-icon">
                  <i class="fas fa-project-diagram"></i>
                </div>
                <span>Simulation Tools</span>
              </div>
              <div class="tech-item">
                <div class="tech-icon">
                  <i class="fas fa-chart-line"></i>
                </div>
                <span>Data Analysis</span>
              </div>
              <div class="tech-item">
                <div class="tech-icon">
                  <i class="fas fa-tools"></i>
                </div>
                <span>Hardware Integration</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'About'
}
</script>

<style scoped>
/* Page Header */
.page-header {
  background: linear-gradient(135deg, var(--primary-color) 0%, #3a4fd7 100%);
  color: white;
  padding: 8rem 0 5rem;
  text-align: center;
}

.page-header h1 {
  font-size: 3rem;
  margin-bottom: 1rem;
}

.page-header p {
  font-size: 1.2rem;
  max-width: 700px;
  margin: 0 auto;
  opacity: 0.9;
}

/* Overview Section */
.overview-content {
  display: grid;
  grid-template-columns: 40% 1fr;
  gap: 3rem;
  align-items: center;
}

.overview-image img {
  width: 100%;
  max-width: 500px;
  height: auto;
  display: block;
}

.overview-text h3 {
  font-size: 1.8rem;
  margin: 1.5rem 0 1rem;
  color: var(--dark-color);
}

.overview-text h3:first-child {
  margin-top: 0;
}

.overview-text p {
  margin-bottom: 1.5rem;
  color: var(--secondary-color);
  line-height: 1.7;
}

.objectives-list {
  list-style: none;
  margin-top: 1.5rem;
}

.objectives-list li {
  display: flex;
  align-items: center;
  margin-bottom: 0.8rem;
  color: var(--secondary-color);
}

.objectives-list li i {
  color: var(--success-color);
  margin-right: 0.8rem;
  font-size: 1.2rem;
}

/* Team Section */
.team-section {
  background-color: var(--light-color);
}

.team-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
}

.team-card {
  background-color: white;
  border-radius: var(--border-radius);
  overflow: hidden;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
  transition: var(--transition);
}

.team-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
}

.team-photo {
  height: 280px;
  overflow: hidden;
}

.team-photo img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.5s ease;
}

.team-card:hover .team-photo img {
  transform: scale(1.05);
}

.team-info {
  padding: 1.5rem;
}

.team-info h3 {
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
}

.team-role {
  color: var(--primary-color);
  font-weight: 600;
  margin-bottom: 1rem;
}

.team-bio {
  color: var(--secondary-color);
  margin-bottom: 1.5rem;
  font-size: 0.95rem;
  line-height: 1.6;
}

.team-social {
  display: flex;
  gap: 1rem;
}

.team-social a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 36px;
  height: 36px;
  border-radius: 50%;
  background-color: rgba(74, 108, 247, 0.1);
  color: var(--primary-color);
  transition: var(--transition);
}

.team-social a:hover {
  background-color: var(--primary-color);
  color: white;
}

/* Methodology Section */
.methodology-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(500px, 1fr));
  gap: 2.5rem;
}

.methodology-item {
  display: flex;
  gap: 1.5rem;
}

.methodology-icon {
  flex-shrink: 0;
  width: 70px;
  height: 70px;
  background-color: rgba(74, 108, 247, 0.1);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.8rem;
  color: var(--primary-color);
}

.methodology-info h3 {
  font-size: 1.5rem;
  margin-bottom: 1rem;
  color: var(--dark-color);
}

.methodology-info p {
  color: var(--secondary-color);
  line-height: 1.7;
}

/* Technologies Section */
.technologies-section {
  background-color: var(--light-color);
}

.tech-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 3rem;
}

.tech-category h3 {
  font-size: 1.8rem;
  margin-bottom: 1.5rem;
  color: var(--dark-color);
  position: relative;
  padding-bottom: 0.8rem;
}

.tech-category h3::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: 0;
  width: 60px;
  height: 3px;
  background-color: var(--primary-color);
}

.tech-list {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.5rem;
}

.tech-item {
  display: flex;
  align-items: center;
  gap: 0.8rem;
}

.tech-icon {
  width: 50px;
  height: 50px;
  background-color: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5rem;
  color: var(--primary-color);
  box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
}

.tech-item span {
  font-weight: 500;
}

/* Responsive Styles */
@media (max-width: 992px) {
  .page-header h1 {
    font-size: 2.5rem;
  }
  
  .overview-content {
    grid-template-columns: 1fr;
  }
  
  .overview-image {
    display: flex;
    justify-content: center;
    margin-bottom: 2rem;
  }
  
  .methodology-content {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 768px) {
  .methodology-item {
    flex-direction: column;
    align-items: flex-start;
  }
  
  .methodology-icon {
    margin-bottom: 1rem;
  }
  
  .tech-list {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 576px) {
  .page-header {
    padding: 6rem 0 3rem;
  }
  
  .page-header h1 {
    font-size: 2rem;
  }
  
  .overview-text h3 {
    font-size: 1.5rem;
  }
  
  .tech-container {
    gap: 2rem;
  }
  
  .tech-category h3 {
    font-size: 1.5rem;
  }
}
</style> 