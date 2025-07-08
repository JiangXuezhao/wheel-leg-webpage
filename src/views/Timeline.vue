<template>
  <div class="timeline-page">
    <!-- Page Header -->
    <section class="page-header">
      <div class="container">
        <h1>Project Timeline</h1>
        <p>Track the development progress of our Wheel-Leg Robot research project</p>
      </div>
    </section>

    <!-- Timeline Section -->
    <section class="section timeline-section">
      <div class="container">
        <!-- Interim Report Section -->
        <div class="interim-report-section">
          <div class="interim-report-header">
            <h2>Interim Report Highlights</h2>
            <p class="report-date">As of June 1, 2025</p>
          </div>
          
          <div class="report-achievements">
            <div class="achievement-grid">
              <div class="achievement-item">
                <div class="achievement-icon">
                  <i class="fas fa-cogs"></i>
                </div>
                <h3>Physical Robot Completed</h3>
                <p>Complete mechanical structures with #-shaped frame, battery, Mini PC, and five-bar linkage joints</p>
              </div>
              
              <div class="achievement-item">
                <div class="achievement-icon">
                  <i class="fas fa-microchip"></i>
                </div>
                <h3>RTOS Control System</h3>
                <p>Unified RTOS project with CAN Bus configuration and joint motor position alignment</p>
              </div>
              
              <div class="achievement-item">
                <div class="achievement-icon">
                  <i class="fas fa-brain"></i>
                </div>
                <h3>PPO Algorithm Training</h3>
                <p>Complete simulation environment with Isaac Gym, testing on flat and complex terrains</p>
              </div>
              
              <div class="achievement-item">
                <div class="achievement-icon">
                  <i class="fas fa-desktop"></i>
                </div>
                <h3>Simulation Platform</h3>
                <p>RTX4070 with Python 3.8, PyTorch 2.3, comprehensive reward function design</p>
              </div>
            </div>
          </div>
        </div>

        <div class="timeline-controls">
          <div class="timeline-filter">
            <label for="phase-filter">Filter by Phase:</label>
            <select id="phase-filter" v-model="currentFilter">
              <option value="all">All Phases</option>
              <option value="design">Design</option>
              <option value="development">Development</option>
              <option value="deployment">Deployment</option>
              <option value="testing">Testing</option>
              <option value="documentation">Documentation</option>
            </select>
          </div>
          <div class="timeline-view-toggle">
            <button 
              @click="timelineView = 'vertical'" 
              :class="{ active: timelineView === 'vertical' }"
            >
              <i class="fas fa-grip-lines"></i> Vertical
            </button>
            <button 
              @click="timelineView = 'horizontal'" 
              :class="{ active: timelineView === 'horizontal' }"
            >
              <i class="fas fa-grip-lines-vertical"></i> Horizontal
            </button>
          </div>
        </div>

        <!-- Vertical Timeline -->
        <div v-if="timelineView === 'vertical'" class="timeline-container vertical">
          <div 
            v-for="(item, index) in filteredTimelineItems" 
            :key="index" 
            class="timeline-item"
            :class="{ 'right': index % 2 !== 0, 'completed': item.status === 'completed', 'in-progress': item.status === 'in-progress', 'upcoming': item.status === 'upcoming' }"
          >
            <div class="timeline-dot"></div>
            <div class="timeline-date">{{ item.date }}</div>
            <div class="timeline-content">
              <div class="timeline-item-status">
                <span :class="item.status">{{ formatStatus(item.status) }}</span>
              </div>
              <h3>{{ item.title }}</h3>
              <div class="timeline-phase">{{ item.phase }}</div>
              <p>{{ item.description }}</p>
              <div v-if="item.deliverables && item.deliverables.length > 0" class="timeline-deliverables">
                <h4>Deliverables:</h4>
                <ul>
                  <li v-for="(deliverable, dIndex) in item.deliverables" :key="dIndex">
                    <i class="fas fa-file-alt"></i> {{ deliverable }}
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>

        <!-- Horizontal Timeline -->
        <div v-else class="timeline-container horizontal">
          <div class="timeline-horizontal-line"></div>
          <div class="timeline-horizontal-items">
            <div 
              v-for="(item, index) in filteredTimelineItems" 
              :key="index" 
              class="timeline-horizontal-item"
              :class="{ 'completed': item.status === 'completed', 'in-progress': item.status === 'in-progress', 'upcoming': item.status === 'upcoming' }"
            >
              <div class="timeline-h-dot"></div>
              <div class="timeline-h-content">
                <div class="timeline-item-status">
                  <span :class="item.status">{{ formatStatus(item.status) }}</span>
                </div>
                <h3>{{ item.title }}</h3>
                <div class="timeline-date">{{ item.date }}</div>
                <div class="timeline-phase">{{ item.phase }}</div>
                <p>{{ item.description }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Project Overview Stats -->
    <section class="section stats-section">
      <div class="container">
        <div class="section-title">
          <h2>Research Progress</h2>
          <p>Current status of our Wheel-Leg Robot development</p>
        </div>
        
        <div class="stats-container">
          <div class="stat-card">
            <div class="stat-icon">
              <i class="fas fa-check-circle"></i>
            </div>
            <div class="stat-info">
              <h3>{{ completedTasks }}</h3>
              <p>Completed Milestones</p>
            </div>
          </div>
          
          <div class="stat-card">
            <div class="stat-icon">
              <i class="fas fa-spinner"></i>
            </div>
            <div class="stat-info">
              <h3>{{ inProgressTasks }}</h3>
              <p>In Progress</p>
            </div>
          </div>
          
          <div class="stat-card">
            <div class="stat-icon">
              <i class="fas fa-hourglass-half"></i>
            </div>
            <div class="stat-info">
              <h3>{{ upcomingTasks }}</h3>
              <p>Upcoming</p>
            </div>
          </div>
          
          <div class="stat-card">
            <div class="stat-icon">
              <i class="fas fa-percentage"></i>
            </div>
            <div class="stat-info">
              <h3>{{ completionPercentage }}%</h3>
              <p>Overall Progress</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'Timeline',
  data() {
    return {
      timelineView: 'vertical',
      currentFilter: 'all',
      timelineItems: [
        {
          title: 'Mechanical Structures Design & Construction',
          date: 'April 1 - May 15, 2025',
          description: 'Complete SolidWorks modeling and physical robot construction. Features #-shaped frame with battery and Mini PC, five-bar linkage joints with hip joint motors and wheel motors.',
          status: 'completed',
          phase: 'Design',
          deliverables: ['SolidWorks 3D Models', 'Physical Robot Prototype', 'Assembly Documentation']
        },
        {
          title: 'Electrical Control System Development',
          date: 'April 15 - May 25, 2025',
          description: 'Implementation of unified RTOS-based control system with CAN Bus configuration and joint motor position alignment. System enables real-time motor control and sensor integration.',
          status: 'completed',
          phase: 'Development',
          deliverables: ['RTOS Control System', 'CAN Bus Configuration', 'Motor Control Interface']
        },
        {
          title: 'Simulation Environment Setup',
          date: 'May 1 - May 30, 2025',
          description: 'Complete Isaac Gym simulation environment setup on RTX4070 with Python 3.8, PyTorch 2.3, CUDA 12.4. Includes state space definition, motion space definition, and reward function design.',
          status: 'completed',
          phase: 'Development',
          deliverables: ['Isaac Gym Environment', 'State/Motion Space Definition', 'Reward Function Framework']
        },
        {
          title: 'Deep Reinforcement Learning Algorithm Implementation',
          date: 'May 20 - June 1, 2025',
          description: 'PPO algorithm implementation with comprehensive reward function design. Training completed on both flat and complex terrains with energy consumption optimization.',
          status: 'completed',
          phase: 'Development',
          deliverables: ['PPO Algorithm Implementation', 'Reward Function Design', 'Training Results on Multiple Terrains']
        },
        {
          title: 'Project Web Page Development',
          date: 'April 18, 2025 - Ongoing',
          description: 'Creation of comprehensive project web pages to showcase the research progress and results. Continually updated throughout the project.',
          status: 'in-progress',
          phase: 'Documentation',
          deliverables: ['Web Application', 'Interactive Visualizations', 'Progress Updates']
        },
        {
          title: 'RTOS Project Finalization & Cable Management',
          date: 'June 1 - June 15, 2025',
          description: 'Completing the unified RTOS project and implementing proper cable management for improved system reliability.',
          status: 'in-progress',
          phase: 'Development',
          deliverables: ['Finalized RTOS System', 'Cable Management Implementation']
        },
        {
          title: 'Simulation Model Integration',
          date: 'June 15 - June 30, 2025',
          description: 'Integration of simulation model with physical robot, including noise perturbation for robustness testing and network parameter optimization.',
          status: 'upcoming',
          phase: 'Development',
          deliverables: ['Simulation-Physical Integration', 'Robustness Testing Results', 'Optimized Network Parameters']
        },
        {
          title: 'Real-world Deployment & Testing',
          date: 'July 1 - July 10, 2025',
          description: 'Packaging neural network for deployment using pkl, jit formats with Docker and ROS2 interface. Testing robot performance in real-world environments.',
          status: 'upcoming',
          phase: 'Testing',
          deliverables: ['Deployment Package', 'Real-world Test Results', 'Performance Analysis']
        },
        {
          title: 'Final Report & Documentation',
          date: 'July 10 - July 15, 2025',
          description: 'Compilation and submission of final project report documenting all aspects of the research including mechanical design, control systems, and DRL implementation.',
          status: 'upcoming',
          phase: 'Documentation',
          deliverables: ['Final Research Report', 'Technical Documentation', 'Project Presentation']
        }
      ]
    }
  },
  computed: {
    filteredTimelineItems() {
      if (this.currentFilter === 'all') {
        return this.timelineItems
      } else {
        return this.timelineItems.filter(item => 
          item.phase.toLowerCase() === this.currentFilter.toLowerCase()
        )
      }
    },
    completedTasks() {
      return this.timelineItems.filter(item => item.status === 'completed').length
    },
    inProgressTasks() {
      return this.timelineItems.filter(item => item.status === 'in-progress').length
    },
    upcomingTasks() {
      return this.timelineItems.filter(item => item.status === 'upcoming').length
    },
    completionPercentage() {
      return Math.round((this.completedTasks / this.timelineItems.length) * 100)
    }
  },
  methods: {
    formatStatus(status) {
      switch (status) {
        case 'completed':
          return 'Completed'
        case 'in-progress':
          return 'In Progress'
        case 'upcoming':
          return 'Upcoming'
        default:
          return status
      }
    }
  }
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

/* Interim Report Section */
.interim-report-section {
  background-color: var(--light-color);
  padding: 4rem 0;
  margin-bottom: 3rem;
  border-radius: var(--border-radius);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
}

.interim-report-header {
  text-align: center;
  margin-bottom: 3rem;
}

.interim-report-header h2 {
  font-size: 2.5rem;
  margin-bottom: 0.5rem;
  color: var(--dark-color);
}

.report-date {
  font-size: 1.1rem;
  color: var(--secondary-color);
  margin-bottom: 2rem;
}

.report-achievements {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: center;
}

.achievement-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
  width: 100%;
}

.achievement-item {
  background-color: white;
  padding: 2rem;
  border-radius: var(--border-radius);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  transition: var(--transition);
}

.achievement-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
}

.achievement-icon {
  width: 80px;
  height: 80px;
  background-color: rgba(74, 108, 247, 0.1);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2.5rem;
  color: var(--primary-color);
  margin-bottom: 1.5rem;
}

.achievement-item h3 {
  font-size: 1.8rem;
  margin-bottom: 0.8rem;
  color: var(--dark-color);
}

.achievement-item p {
  font-size: 1rem;
  color: var(--secondary-color);
  line-height: 1.6;
}

/* Timeline Controls */
.timeline-controls {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 3rem;
}

.timeline-filter label {
  margin-right: 0.5rem;
  font-weight: 500;
}

.timeline-filter select {
  padding: 0.5rem 1rem;
  border: 1px solid var(--border-color);
  border-radius: 5px;
  background-color: white;
  cursor: pointer;
}

.timeline-view-toggle {
  display: flex;
  gap: 0.5rem;
}

.timeline-view-toggle button {
  background-color: white;
  border: 1px solid var(--border-color);
  border-radius: 5px;
  padding: 0.5rem 1rem;
  cursor: pointer;
  transition: var(--transition);
}

.timeline-view-toggle button.active {
  background-color: var(--primary-color);
  color: white;
  border-color: var(--primary-color);
}

/* Vertical Timeline */
.timeline-container.vertical {
  position: relative;
  max-width: 1000px;
  margin: 0 auto;
}

.timeline-container.vertical::after {
  content: '';
  position: absolute;
  width: 4px;
  background-color: var(--border-color);
  top: 0;
  bottom: 0;
  left: 50%;
  margin-left: -2px;
}

.timeline-item {
  padding: 10px 40px;
  position: relative;
  width: 50%;
  box-sizing: border-box;
  margin-bottom: 3rem;
}

.timeline-item::after {
  content: '';
  position: absolute;
  width: 20px;
  height: 20px;
  right: -10px;
  top: 15px;
  border-radius: 50%;
  z-index: 1;
}

.timeline-item.right {
  left: 50%;
}

.timeline-item.right::after {
  left: -10px;
}

.timeline-dot {
  position: absolute;
  width: 25px;
  height: 25px;
  right: -12.5px;
  background-color: white;
  border: 4px solid var(--primary-color);
  top: 15px;
  border-radius: 50%;
  z-index: 2;
}

.timeline-item.right .timeline-dot {
  left: -12.5px;
}

.timeline-date {
  position: absolute;
  top: 0;
  right: calc(100% + 20px);
  font-weight: 600;
  color: var(--secondary-color);
  width: 120px;
  text-align: right;
}

.timeline-item.right .timeline-date {
  left: calc(100% + 20px);
  right: auto;
  text-align: left;
}

.timeline-content {
  padding: 1.5rem;
  background-color: white;
  position: relative;
  border-radius: var(--border-radius);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
  transition: var(--transition);
}

.timeline-content:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
}

.timeline-content::after {
  content: '';
  position: absolute;
  border-style: solid;
  border-width: 10px 0 10px 10px;
  border-color: transparent transparent transparent white;
  top: 15px;
  right: -10px;
}

.timeline-item.right .timeline-content::after {
  border-width: 10px 10px 10px 0;
  border-color: transparent white transparent transparent;
  left: -10px;
  right: auto;
}

.timeline-item-status {
  margin-bottom: 0.5rem;
}

.timeline-item-status span {
  display: inline-block;
  padding: 0.3rem 0.8rem;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: 500;
}

span.completed {
  background-color: rgba(40, 167, 69, 0.1);
  color: var(--success-color);
}

span.in-progress {
  background-color: rgba(255, 193, 7, 0.1);
  color: var(--warning-color);
}

span.upcoming {
  background-color: rgba(23, 162, 184, 0.1);
  color: var(--info-color);
}

.timeline-content h3 {
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
}

.timeline-phase {
  font-size: 0.9rem;
  color: var(--primary-color);
  font-weight: 600;
  margin-bottom: 1rem;
}

.timeline-content p {
  margin-bottom: 1rem;
  color: var(--secondary-color);
}

.timeline-deliverables h4 {
  font-size: 1rem;
  margin-bottom: 0.5rem;
}

.timeline-deliverables ul {
  list-style: none;
}

.timeline-deliverables li {
  display: flex;
  align-items: center;
  margin-bottom: 0.5rem;
  font-size: 0.9rem;
  color: var(--secondary-color);
}

.timeline-deliverables li i {
  margin-right: 0.5rem;
  color: var(--primary-color);
}

/* Horizontal Timeline */
.timeline-container.horizontal {
  position: relative;
  padding: 2rem 0;
  overflow-x: auto;
}

.timeline-horizontal-line {
  position: absolute;
  height: 4px;
  background-color: var(--border-color);
  top: 90px;
  left: 0;
  right: 0;
}

.timeline-horizontal-items {
  display: flex;
  min-width: max-content;
  padding: 2rem 0;
}

.timeline-horizontal-item {
  position: relative;
  margin-right: 5rem;
  min-width: 250px;
}

.timeline-h-dot {
  position: absolute;
  width: 25px;
  height: 25px;
  background-color: white;
  border: 4px solid var(--primary-color);
  border-radius: 50%;
  top: 80px;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 2;
}

.timeline-h-content {
  background-color: white;
  padding: 1.5rem;
  border-radius: var(--border-radius);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
  margin-top: 5rem;
  transition: var(--transition);
}

.timeline-h-content:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
}

/* Stats Section */
.stats-section {
  background-color: var(--light-color);
}

.stats-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 2rem;
}

.stat-card {
  background-color: white;
  padding: 2rem;
  border-radius: var(--border-radius);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
  display: flex;
  align-items: center;
  transition: var(--transition);
}

.stat-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
}

.stat-icon {
  width: 70px;
  height: 70px;
  background-color: rgba(74, 108, 247, 0.1);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.8rem;
  color: var(--primary-color);
  margin-right: 1.5rem;
}

.stat-info h3 {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 0.3rem;
  color: var(--dark-color);
}

.stat-info p {
  color: var(--secondary-color);
  font-size: 1rem;
}

/* Responsive Styles */
@media (max-width: 992px) {
  .page-header h1 {
    font-size: 2.5rem;
  }
}

@media (max-width: 768px) {
  .timeline-controls {
    flex-direction: column;
    gap: 1rem;
    align-items: flex-start;
  }
  
  .timeline-container.vertical::after {
    left: 40px;
  }
  
  .timeline-item {
    width: 100%;
    padding-left: 80px;
    padding-right: 0;
  }
  
  .timeline-item.right {
    left: 0;
  }
  
  .timeline-dot {
    left: 27.5px;
    right: auto;
  }
  
  .timeline-item.right .timeline-dot {
    left: 27.5px;
  }
  
  .timeline-date {
    right: auto;
    left: 0;
    top: -30px;
    text-align: left;
    width: auto;
  }
  
  .timeline-item.right .timeline-date {
    right: auto;
    left: 0;
    text-align: left;
  }
  
  .timeline-content::after {
    border-width: 10px 10px 10px 0;
    border-color: transparent white transparent transparent;
    left: -10px;
    right: auto;
  }
  
  .timeline-item.right .timeline-content::after {
    border-width: 10px 10px 10px 0;
    border-color: transparent white transparent transparent;
    left: -10px;
    right: auto;
  }
}

@media (max-width: 576px) {
  .page-header {
    padding: 6rem 0 3rem;
  }
  
  .page-header h1 {
    font-size: 2rem;
  }
  
  .timeline-item {
    padding-left: 60px;
  }
  
  .timeline-container.vertical::after {
    left: 20px;
  }
  
  .timeline-dot {
    left: 7.5px;
  }
  
  .timeline-item.right .timeline-dot {
    left: 7.5px;
  }
  
  .stat-card {
    flex-direction: column;
    text-align: center;
  }
  
  .stat-icon {
    margin-right: 0;
    margin-bottom: 1rem;
  }
}
</style> 