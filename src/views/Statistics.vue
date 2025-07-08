<template>
  <div class="statistics-page">
    <!-- Page Header -->
    <section class="page-header">
      <div class="container">
        <h1>Project Statistics</h1>
        <p>Analytical insights and metrics about our Wheel-Leg Robot research project</p>
      </div>
    </section>

    <!-- Overall Progress Section -->
    <section class="section progress-section">
      <div class="container">
        <div class="section-title">
          <h2>Overall Progress</h2>
          <p>Current progress metrics across different aspects of the project</p>
        </div>

        <div class="progress-cards">
          <div class="progress-card">
            <h3>Overall Completion</h3>
            <div class="progress-container">
              <div class="progress-circle" :style="{ '--progress': '85%' }">
                <div class="progress-circle-inner">
                  <span>85%</span>
                </div>
              </div>
            </div>
            <p>Significant progress made through June 30, 2025</p>
          </div>

          <div class="progress-card">
            <h3>Tasks Completion</h3>
            <div class="progress-bar-container">
              <div class="progress-label">
                <span>Completed</span>
                <span>8/11</span>
              </div>
              <div class="progress-bar">
                <div class="progress" style="width: 72.7%;"></div>
              </div>
            </div>
            <div class="progress-bar-container">
              <div class="progress-label">
                <span>In Progress</span>
                <span>1/11</span>
              </div>
              <div class="progress-bar">
                <div class="progress in-progress" style="width: 9.1%;"></div>
              </div>
            </div>
            <div class="progress-bar-container">
              <div class="progress-label">
                <span>Pending</span>
                <span>2/11</span>
              </div>
              <div class="progress-bar">
                <div class="progress pending" style="width: 18.2%;"></div>
              </div>
            </div>
          </div>

          <div class="progress-card">
            <h3>Timeline Status</h3>
            <div class="timeline-status">
              <div class="status-item">
                <i class="fas fa-clock"></i>
                <div class="status-details">
                  <h4>Project Duration</h4>
                  <p>4 months (April - July 2025)</p>
                </div>
              </div>
              <div class="status-item">
                <i class="fas fa-calendar-check"></i>
                <div class="status-details">
                  <h4>Time Elapsed</h4>
                  <p>3 months (75%)</p>
                </div>
              </div>
              <div class="status-item">
                <i class="fas fa-calendar-day"></i>
                <div class="status-details">
                  <h4>Time Remaining</h4>
                  <p>2 weeks</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Phase Progress Section -->
    <section class="section phase-section">
      <div class="container">
        <div class="section-title">
          <h2>Phase Progress</h2>
          <p>Detailed progress breakdown by project phase</p>
        </div>

        <div class="phase-progress">
          <div class="phase-card">
            <div class="phase-header">
              <h3>Design</h3>
              <span class="phase-status completed">Completed</span>
            </div>
            <div class="phase-progress-bar">
              <div class="phase-progress-indicator" style="width: 100%;"></div>
            </div>
            <div class="phase-stats">
              <div class="phase-stat">
                <span>Start Date</span>
                <span>Apr 1, 2025</span>
              </div>
              <div class="phase-stat">
                <span>End Date</span>
                <span>May 15, 2025</span>
              </div>
              <div class="phase-stat">
                <span>Tasks</span>
                <span>1/1 Completed</span>
              </div>
            </div>
          </div>

          <div class="phase-card">
            <div class="phase-header">
              <h3>Development</h3>
              <span class="phase-status completed">Completed</span>
            </div>
            <div class="phase-progress-bar">
              <div class="phase-progress-indicator" style="width: 100%;"></div>
            </div>
            <div class="phase-stats">
              <div class="phase-stat">
                <span>Start Date</span>
                <span>Apr 15, 2025</span>
              </div>
              <div class="phase-stat">
                <span>End Date</span>
                <span>Jun 30, 2025</span>
              </div>
              <div class="phase-stat">
                <span>Tasks</span>
                <span>7/7 Completed</span>
              </div>
            </div>
          </div>

          <div class="phase-card">
            <div class="phase-header">
              <h3>Documentation</h3>
              <span class="phase-status in-progress">In Progress</span>
            </div>
            <div class="phase-progress-bar">
              <div class="phase-progress-indicator" style="width: 60%;"></div>
            </div>
            <div class="phase-stats">
              <div class="phase-stat">
                <span>Start Date</span>
                <span>Apr 18, 2025</span>
              </div>
              <div class="phase-stat">
                <span>End Date</span>
                <span>Jul 15, 2025</span>
              </div>
              <div class="phase-stat">
                <span>Tasks</span>
                <span>1/2 In Progress</span>
              </div>
            </div>
          </div>

          <div class="phase-card">
            <div class="phase-header">
              <h3>Testing</h3>
              <span class="phase-status upcoming">Upcoming</span>
            </div>
            <div class="phase-progress-bar">
              <div class="phase-progress-indicator" style="width: 0%;"></div>
            </div>
            <div class="phase-stats">
              <div class="phase-stat">
                <span>Start Date</span>
                <span>Jul 1, 2025</span>
              </div>
              <div class="phase-stat">
                <span>End Date</span>
                <span>Jul 10, 2025</span>
              </div>
              <div class="phase-stat">
                <span>Tasks</span>
                <span>0/1 Completed</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Resource Allocation Section -->
    <section class="section resource-section">
      <div class="container">
        <div class="section-title">
          <h2>Resource Allocation</h2>
          <p>Distribution of resources across different project areas</p>
        </div>

        <div class="resource-cards">
          <div class="resource-card">
            <h3>Team Distribution</h3>
            <div class="pie-chart-container">
              <div class="pie-chart">
                <div class="slice slice1" style="--percentage: 35%; --color: var(--primary-color);"></div>
                <div class="slice slice2" style="--percentage: 30%; --color: #6c757d;"></div>
                <div class="slice slice3" style="--percentage: 20%; --color: #28a745;"></div>
                <div class="slice slice4" style="--percentage: 15%; --color: #17a2b8;"></div>
              </div>
              <div class="pie-legend">
                <div class="legend-item">
                  <span class="legend-color" style="background-color: var(--primary-color);"></span>
                  <span>Robot Design (35%)</span>
                </div>
                <div class="legend-item">
                  <span class="legend-color" style="background-color: #6c757d;"></span>
                  <span>Control Systems (30%)</span>
                </div>
                <div class="legend-item">
                  <span class="legend-color" style="background-color: #28a745;"></span>
                  <span>DRL Implementation (20%)</span>
                </div>
                <div class="legend-item">
                  <span class="legend-color" style="background-color: #17a2b8;"></span>
                  <span>Documentation (15%)</span>
                </div>
              </div>
            </div>
          </div>

          <div class="resource-card">
            <h3>Learning Hours Allocation</h3>
            <div class="pie-chart-container">
              <div class="pie-chart">
                <div class="slice slice1" style="--percentage: 27%; --color: var(--primary-color);"></div>
                <div class="slice slice2" style="--percentage: 13%; --color: #6c757d;"></div>
                <div class="slice slice3" style="--percentage: 40%; --color: #28a745;"></div>
                <div class="slice slice4" style="--percentage: 20%; --color: #17a2b8;"></div>
              </div>
              <div class="pie-legend">
                <div class="legend-item">
                  <span class="legend-color" style="background-color: var(--primary-color);"></span>
                  <span>Robot Design (20 hrs, 7%)</span>
                </div>
                <div class="legend-item">
                  <span class="legend-color" style="background-color: #6c757d;"></span>
                  <span>Control System (40 hrs, 13%)</span>
                </div>
                <div class="legend-item">
                  <span class="legend-color" style="background-color: #28a745;"></span>
                  <span>DRL Training (120 hrs, 40%)</span>
                </div>
                <div class="legend-item">
                  <span class="legend-color" style="background-color: #17a2b8;"></span>
                  <span>Edge Computing & Testing (60 hrs, 20%)</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Key Performance Indicators -->
    <section class="section kpi-section">
      <div class="container">
        <div class="section-title">
          <h2>Key Performance Indicators</h2>
          <p>Critical metrics tracking our Wheel-Leg Robot research progress</p>
        </div>

        <div class="kpi-cards">
          <div class="kpi-card">
            <div class="kpi-icon">
              <i class="fas fa-robot"></i>
            </div>
            <div class="kpi-content">
              <h3>Control System Accuracy</h3>
              <div class="kpi-value">
                <span>85%</span>
                <span class="kpi-unit">Precision</span>
              </div>
              <div class="kpi-trend positive">
                <i class="fas fa-arrow-up"></i>
                <span>12% from baseline</span>
              </div>
            </div>
          </div>

          <div class="kpi-card">
            <div class="kpi-icon">
              <i class="fas fa-cogs"></i>
            </div>
            <div class="kpi-content">
              <h3>Robot Movement Efficiency</h3>
              <div class="kpi-value">
                <span>0.78</span>
                <span class="kpi-unit">Energy/Distance</span>
              </div>
              <div class="kpi-trend positive">
                <i class="fas fa-arrow-up"></i>
                <span>15% improvement</span>
              </div>
            </div>
          </div>

          <div class="kpi-card">
            <div class="kpi-icon">
              <i class="fas fa-microchip"></i>
            </div>
            <div class="kpi-content">
              <h3>DRL Model Performance</h3>
              <div class="kpi-value">
                <span>72%</span>
              </div>
              <div class="kpi-trend positive">
                <i class="fas fa-arrow-up"></i>
                <span>8% from last iteration</span>
              </div>
            </div>
          </div>

          <div class="kpi-card">
            <div class="kpi-icon">
              <i class="fas fa-stopwatch"></i>
            </div>
            <div class="kpi-content">
              <h3>Processing Latency</h3>
              <div class="kpi-value">
                <span>24</span>
                <span class="kpi-unit">ms</span>
              </div>
              <div class="kpi-trend positive">
                <i class="fas fa-arrow-down"></i>
                <span>35% reduction</span>
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
  name: 'Statistics'
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

/* Progress Section */
.progress-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.progress-card {
  background-color: white;
  padding: 2rem;
  border-radius: var(--border-radius);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
  transition: var(--transition);
}

.progress-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
}

.progress-card h3 {
  font-size: 1.5rem;
  margin-bottom: 1.5rem;
  position: relative;
}

.progress-card h3::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: -10px;
  width: 50px;
  height: 3px;
  background-color: var(--primary-color);
}

.progress-card p {
  margin-top: 1rem;
  color: var(--secondary-color);
}

/* Progress Circle */
.progress-container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 2rem 0;
}

.progress-circle {
  width: 200px;
  height: 200px;
  border-radius: 50%;
  background: conic-gradient(var(--primary-color) 0% var(--progress), #e9ecef var(--progress) 100%);
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
}

.progress-circle::before {
  content: '';
  position: absolute;
  width: 160px;
  height: 160px;
  border-radius: 50%;
  background-color: white;
}

.progress-circle-inner {
  z-index: 2;
  font-size: 2.5rem;
  font-weight: 700;
  color: var(--primary-color);
}

/* Progress Bars */
.progress-bar-container {
  margin-bottom: 1.5rem;
}

.progress-label {
  display: flex;
  justify-content: space-between;
  margin-bottom: 0.5rem;
  font-size: 0.9rem;
  color: var(--secondary-color);
}

.progress-bar {
  height: 10px;
  background-color: var(--border-color);
  border-radius: 5px;
  overflow: hidden;
}

.progress {
  height: 100%;
  background-color: var(--primary-color);
  border-radius: 5px;
}

.progress.in-progress {
  background-color: var(--warning-color);
}

.progress.pending {
  background-color: var(--secondary-color);
}

/* Timeline Status */
.timeline-status {
  margin-top: 2rem;
}

.status-item {
  display: flex;
  align-items: center;
  margin-bottom: 1.5rem;
}

.status-item i {
  font-size: 1.8rem;
  color: var(--primary-color);
  margin-right: 1.5rem;
  width: 40px;
  text-align: center;
}

.status-details h4 {
  font-size: 1.1rem;
  margin-bottom: 0.3rem;
}

.status-details p {
  margin-top: 0;
  font-size: 1.2rem;
  font-weight: 600;
}

/* Phase Progress */
.phase-section {
  background-color: var(--light-color);
}

.phase-progress {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.phase-card {
  background-color: white;
  padding: 1.5rem;
  border-radius: var(--border-radius);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
  transition: var(--transition);
}

.phase-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
}

.phase-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1.5rem;
}

.phase-header h3 {
  font-size: 1.3rem;
  margin: 0;
}

.phase-status {
  padding: 0.3rem 0.8rem;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: 500;
}

.phase-status.completed {
  background-color: rgba(40, 167, 69, 0.1);
  color: var(--success-color);
}

.phase-status.in-progress {
  background-color: rgba(255, 193, 7, 0.1);
  color: var(--warning-color);
}

.phase-status.upcoming {
  background-color: rgba(23, 162, 184, 0.1);
  color: var(--info-color);
}

.phase-progress-bar {
  height: 8px;
  background-color: var(--border-color);
  border-radius: 4px;
  overflow: hidden;
  margin-bottom: 1.5rem;
}

.phase-progress-indicator {
  height: 100%;
  background-color: var(--primary-color);
  border-radius: 4px;
}

.phase-stats {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
}

.phase-stat {
  display: flex;
  flex-direction: column;
}

.phase-stat span:first-child {
  font-size: 0.8rem;
  color: var(--secondary-color);
  margin-bottom: 0.3rem;
}

.phase-stat span:last-child {
  font-weight: 600;
  font-size: 0.9rem;
}

/* Resource Section */
.resource-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
  gap: 2rem;
}

.resource-card {
  background-color: white;
  padding: 2rem;
  border-radius: var(--border-radius);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
  transition: var(--transition);
}

.resource-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
}

.resource-card h3 {
  font-size: 1.5rem;
  margin-bottom: 2rem;
  position: relative;
}

.resource-card h3::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: -10px;
  width: 50px;
  height: 3px;
  background-color: var(--primary-color);
}

/* Pie Chart */
.pie-chart-container {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.pie-chart {
  width: 200px;
  height: 200px;
  border-radius: 50%;
  position: relative;
  margin-bottom: 2rem;
  background-color: #f8f9fa;
}

.slice {
  position: absolute;
  width: 100%;
  height: 100%;
  border-radius: 50%;
  clip: rect(0, 100px, 200px, 0);
}

.slice1 {
  background-color: var(--color);
  clip-path: conic-gradient(var(--color) 0% var(--percentage), transparent var(--percentage) 100%);
}

.slice2 {
  background-color: var(--color);
  clip-path: conic-gradient(transparent 0% var(--percentage-prev, 0%), var(--color) var(--percentage-prev, 0%) calc(var(--percentage-prev, 0%) + var(--percentage)), transparent calc(var(--percentage-prev, 0%) + var(--percentage)) 100%);
  --percentage-prev: 40%;
}

.slice3 {
  background-color: var(--color);
  clip-path: conic-gradient(transparent 0% calc(var(--percentage-prev1, 0%) + var(--percentage-prev2, 0%)), var(--color) calc(var(--percentage-prev1, 0%) + var(--percentage-prev2, 0%)) calc(var(--percentage-prev1, 0%) + var(--percentage-prev2, 0%) + var(--percentage)), transparent calc(var(--percentage-prev1, 0%) + var(--percentage-prev2, 0%) + var(--percentage)) 100%);
  --percentage-prev1: 40%;
  --percentage-prev2: 25%;
}

.slice4 {
  background-color: var(--color);
  clip-path: conic-gradient(transparent 0% calc(var(--percentage-prev1, 0%) + var(--percentage-prev2, 0%) + var(--percentage-prev3, 0%)), var(--color) calc(var(--percentage-prev1, 0%) + var(--percentage-prev2, 0%) + var(--percentage-prev3, 0%)) calc(var(--percentage-prev1, 0%) + var(--percentage-prev2, 0%) + var(--percentage-prev3, 0%) + var(--percentage)), transparent calc(var(--percentage-prev1, 0%) + var(--percentage-prev2, 0%) + var(--percentage-prev3, 0%) + var(--percentage)) 100%);
  --percentage-prev1: 40%;
  --percentage-prev2: 25%;
  --percentage-prev3: 20%;
}

.pie-legend {
  width: 100%;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1rem;
}

.legend-item {
  display: flex;
  align-items: center;
  font-size: 0.9rem;
}

.legend-color {
  width: 15px;
  height: 15px;
  border-radius: 3px;
  margin-right: 0.5rem;
}

/* KPI Section */
.kpi-section {
  background-color: var(--light-color);
}

.kpi-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.kpi-card {
  background-color: white;
  padding: 2rem;
  border-radius: var(--border-radius);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
  display: flex;
  align-items: flex-start;
  transition: var(--transition);
}

.kpi-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
}

.kpi-icon {
  width: 60px;
  height: 60px;
  background-color: rgba(74, 108, 247, 0.1);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5rem;
  color: var(--primary-color);
  margin-right: 1.5rem;
}

.kpi-content {
  flex: 1;
}

.kpi-content h3 {
  font-size: 1.1rem;
  margin-bottom: 0.8rem;
}

.kpi-value {
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
  color: var(--dark-color);
  display: flex;
  align-items: baseline;
}

.kpi-unit {
  font-size: 0.9rem;
  font-weight: 400;
  color: var(--secondary-color);
  margin-left: 0.5rem;
}

.kpi-trend {
  font-size: 0.9rem;
  display: flex;
  align-items: center;
}

.kpi-trend i {
  margin-right: 0.3rem;
}

.kpi-trend.positive {
  color: var(--success-color);
}

.kpi-trend.negative {
  color: var(--danger-color);
}

/* Responsive Styles */
@media (max-width: 992px) {
  .page-header h1 {
    font-size: 2.5rem;
  }
  
  .resource-cards {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 768px) {
  .phase-stats {
    grid-template-columns: 1fr;
  }
  
  .pie-legend {
    grid-template-columns: 1fr;
  }
  
  .kpi-card {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
  
  .kpi-icon {
    margin-right: 0;
    margin-bottom: 1.5rem;
  }
  
  .kpi-value {
    justify-content: center;
  }
  
  .kpi-trend {
    justify-content: center;
  }
}

@media (max-width: 576px) {
  .page-header {
    padding: 6rem 0 3rem;
  }
  
  .page-header h1 {
    font-size: 2rem;
  }
  
  .progress-circle {
    width: 160px;
    height: 160px;
  }
  
  .progress-circle::before {
    width: 120px;
    height: 120px;
  }
  
  .progress-circle-inner {
    font-size: 2rem;
  }
}
</style> 