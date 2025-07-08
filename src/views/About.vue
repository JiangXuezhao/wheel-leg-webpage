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

    <!-- Technical Specifications Section -->
    <section class="section technical-specs-section">
      <div class="container">
        <div class="section-title">
          <h2>Technical Specifications</h2>
          <p>Detailed technical information about our implementation (as of June 1, 2025)</p>
        </div>

        <div class="specs-content">
          <div class="specs-card">
            <div class="specs-header">
              <i class="fas fa-cogs"></i>
              <h3>Mechanical Structure</h3>
            </div>
            <div class="specs-details">
              <div class="spec-item">
                <span class="spec-label">Frame Design:</span>
                <span class="spec-value">#-shaped frame with integrated battery and Mini PC</span>
              </div>
              <div class="spec-item">
                <span class="spec-label">Leg Design:</span>
                <span class="spec-value">Hip joint motor + Five-bar linkage joint + Wheel motor</span>
              </div>
              <div class="spec-item">
                <span class="spec-label">Modeling Platform:</span>
                <span class="spec-value">SolidWorks (Complete 3D modeling)</span>
              </div>
              <div class="spec-item">
                <span class="spec-label">Status:</span>
                <span class="spec-value status-completed">Physical assembly completed</span>
              </div>
            </div>
          </div>

          <div class="specs-card">
            <div class="specs-header">
              <i class="fas fa-microchip"></i>
              <h3>Electrical Control</h3>
            </div>
            <div class="specs-details">
              <div class="spec-item">
                <span class="spec-label">Communication:</span>
                <span class="spec-value">CAN Bus configuration implemented</span>
              </div>
              <div class="spec-item">
                <span class="spec-label">Motor Control:</span>
                <span class="spec-value">Joint motor position alignment complete</span>
              </div>
              <div class="spec-item">
                <span class="spec-label">Control System:</span>
                <span class="spec-value">RTOS-based unified project</span>
              </div>
              <div class="spec-item">
                <span class="spec-label">Status:</span>
                <span class="spec-value status-completed">Core system operational</span>
              </div>
            </div>
          </div>

          <div class="specs-card">
            <div class="specs-header">
              <i class="fas fa-desktop"></i>
              <h3>Simulation Environment</h3>
            </div>
            <div class="specs-details">
              <div class="spec-item">
                <span class="spec-label">Hardware:</span>
                <span class="spec-value">AMD R9-7949HX, NVIDIA RTX4070</span>
              </div>
              <div class="spec-item">
                <span class="spec-label">Platform:</span>
                <span class="spec-value">Isaac Gym</span>
              </div>
              <div class="spec-item">
                <span class="spec-label">Software Stack:</span>
                <span class="spec-value">Python 3.8, PyTorch 2.3, CUDA 12.4</span>
              </div>
              <div class="spec-item">
                <span class="spec-label">Status:</span>
                <span class="spec-value status-completed">Fully operational</span>
              </div>
            </div>
          </div>

          <div class="specs-card">
            <div class="specs-header">
              <i class="fas fa-brain"></i>
              <h3>Deep Reinforcement Learning</h3>
            </div>
            <div class="specs-details">
              <div class="spec-item">
                <span class="spec-label">Algorithm:</span>
                <span class="spec-value">PPO (Proximal Policy Optimization)</span>
              </div>
              <div class="spec-item">
                <span class="spec-label">Network:</span>
                <span class="spec-value">Actor-Critic MLP architecture</span>
              </div>
              <div class="spec-item">
                <span class="spec-label">State Space:</span>
                <span class="spec-value">30 dimensions (velocity, gravity, commands, joints)</span>
              </div>
              <div class="spec-item">
                <span class="spec-label">Action Space:</span>
                <span class="spec-value">6 dimensions (joint target positions/velocities)</span>
              </div>
              <div class="spec-item">
                <span class="spec-label">Terrain Testing:</span>
                <span class="spec-value">Flat terrain and complex terrain completed</span>
              </div>
              <div class="spec-item">
                <span class="spec-label">Status:</span>
                <span class="spec-value status-completed">Training completed</span>
              </div>
            </div>
          </div>
        </div>

        <div class="reward-function-section">
          <h3>Reward Function Design</h3>
          <p>Our comprehensive reward function optimizes multiple aspects of robot behavior:</p>
          <div class="reward-categories">
            <div class="reward-category">
              <h4>Tracking Rewards</h4>
              <ul>
                <li>Linear velocity tracking: exp(-error²/0.25)</li>
                <li>Angular velocity tracking: exp(-error²/0.25)</li>
                <li>Height control: exp(-error²/0.001)</li>
              </ul>
            </div>
            <div class="reward-category">
              <h4>Stability Penalties</h4>
              <ul>
                <li>Vertical velocity: -2.0 × vz²</li>
                <li>Angular velocity: -0.05 × ω_xy²</li>
                <li>Orientation: -10.0 × gravity_projection²</li>
              </ul>
            </div>
            <div class="reward-category">
              <h4>Energy & Joint Control</h4>
              <ul>
                <li>Torque optimization</li>
                <li>Power consumption minimization</li>
                <li>Joint velocity and acceleration limits</li>
                <li>Action smoothness enforcement</li>
              </ul>
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
                We have completed the design and construction of a five-link balanced wheel leg structure with #-shaped frame, 
                integrated battery, and Mini PC. The modeling was performed using SolidWorks, with thorough verification of the 
                structure's strength and stiffness. All hardware components have been carefully selected and integrated to ensure 
                optimal performance.
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
                Our control system has been successfully implemented using RTOS-based unified project architecture. We have 
                completed CAN Bus configuration and joint motor position alignment. The system enables real-time sensor data 
                processing and motor control with efficient communication protocols.
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
                We have constructed a comprehensive simulation environment using Isaac Gym with detailed state and motion space 
                definitions. Our PPO algorithm implementation includes carefully designed reward functions optimizing velocity 
                tracking, stability, and energy consumption. Training has been completed on both flat and complex terrains.
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
                We have completed initial testing in simulation environments across different terrain types. Our evaluation 
                includes metrics like speed, stability, and energy consumption. Current focus is on real-world deployment 
                preparation and system integration testing.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Future Plans Section -->
    <section class="section future-plans-section">
      <div class="container">
        <div class="section-title">
          <h2>Future Plans</h2>
          <p>Upcoming work and development roadmap</p>
        </div>

        <div class="future-plans-content">
          <div class="plan-item">
            <div class="plan-icon">
              <i class="fas fa-wrench"></i>
            </div>
            <div class="plan-info">
              <h3>System Finalization</h3>
              <p>Complete the unified RTOS project and implement comprehensive cable management for improved system reliability and maintenance.</p>
            </div>
          </div>

          <div class="plan-item">
            <div class="plan-icon">
              <i class="fas fa-link"></i>
            </div>
            <div class="plan-info">
              <h3>Simulation-Physical Integration</h3>
              <p>Establish cooperation between simulation model and physical robot to enable seamless transfer of trained policies to real-world applications.</p>
            </div>
          </div>

          <div class="plan-item">
            <div class="plan-icon">
              <i class="fas fa-shield-alt"></i>
            </div>
            <div class="plan-info">
              <h3>Robustness Enhancement</h3>
              <p>Implement observation perturbation with random noise to improve the robustness of simulation results and real-world performance.</p>
            </div>
          </div>

          <div class="plan-item">
            <div class="plan-icon">
              <i class="fas fa-cog"></i>
            </div>
            <div class="plan-info">
              <h3>Network Optimization</h3>
              <p>Fine-tune neural network parameters through testing on different platforms to achieve optimal computation time and performance balance.</p>
            </div>
          </div>

          <div class="plan-item">
            <div class="plan-icon">
              <i class="fas fa-box"></i>
            </div>
            <div class="plan-info">
              <h3>Deployment Packaging</h3>
              <p>Package the network into .pkl, .jit formats using Docker and ROS2 interface to improve stability and deployment efficiency in real environments.</p>
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

/* Technical Specifications Section */
.technical-specs-section {
  background-color: var(--light-color);
  padding: 5rem 0;
}

.specs-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2.5rem;
  margin-bottom: 3rem;
}

.specs-card {
  background-color: white;
  border-radius: var(--border-radius);
  padding: 2rem;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
  transition: var(--transition);
}

.specs-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
}

.specs-header {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 1.5rem;
  color: var(--primary-color);
}

.specs-header i {
  font-size: 2rem;
}

.specs-header h3 {
  font-size: 1.8rem;
  color: var(--dark-color);
}

.specs-details {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.spec-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.8rem 0;
  border-bottom: 1px solid #eee;
}

.spec-item:last-child {
  border-bottom: none;
}

.spec-label {
  font-weight: 600;
  color: var(--secondary-color);
  font-size: 0.9rem;
}

.spec-value {
  font-weight: 500;
  color: var(--dark-color);
  font-size: 1rem;
}

.status-completed {
  color: var(--success-color);
  font-weight: 600;
}

.reward-function-section {
  background-color: white;
  border-radius: var(--border-radius);
  padding: 2rem;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
}

.reward-function-section h3 {
  font-size: 1.8rem;
  margin-bottom: 1.5rem;
  color: var(--dark-color);
}

.reward-categories {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.reward-category h4 {
  font-size: 1.3rem;
  margin-bottom: 0.8rem;
  color: var(--primary-color);
}

.reward-category ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.reward-category li {
  margin-bottom: 0.5rem;
  color: var(--secondary-color);
  font-size: 1rem;
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

/* Future Plans Section */
.future-plans-section {
  background-color: var(--light-color);
  padding: 5rem 0;
}

.future-plans-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2.5rem;
}

.plan-item {
  background-color: white;
  border-radius: var(--border-radius);
  padding: 2rem;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
  transition: var(--transition);
  display: flex;
  align-items: center;
  gap: 1.5rem;
}

.plan-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
}

.plan-icon {
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

.plan-info h3 {
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
  color: var(--dark-color);
}

.plan-info p {
  color: var(--secondary-color);
  line-height: 1.6;
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