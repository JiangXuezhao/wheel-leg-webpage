<template>
  <div class="statistics-page">
    <!-- Page Header -->
    <section class="page-header">
      <div class="container">
        <h1>Project Statistics</h1>
        <p>Analytical insights and metrics about our project progress</p>
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
              <div class="progress-circle" :style="{ '--progress': '70%' }">
                <div class="progress-circle-inner">
                  <span>70%</span>
                </div>
              </div>
            </div>
            <p>Project is on track to meet the deadline</p>
          </div>

          <div class="progress-card">
            <h3>Tasks Completion</h3>
            <div class="progress-bar-container">
              <div class="progress-label">
                <span>Completed</span>
                <span>28/40</span>
              </div>
              <div class="progress-bar">
                <div class="progress" style="width: 70%;"></div>
              </div>
            </div>
            <div class="progress-bar-container">
              <div class="progress-label">
                <span>In Progress</span>
                <span>8/40</span>
              </div>
              <div class="progress-bar">
                <div class="progress in-progress" style="width: 20%;"></div>
              </div>
            </div>
            <div class="progress-bar-container">
              <div class="progress-label">
                <span>Pending</span>
                <span>4/40</span>
              </div>
              <div class="progress-bar">
                <div class="progress pending" style="width: 10%;"></div>
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
                  <p>12 months</p>
                </div>
              </div>
              <div class="status-item">
                <i class="fas fa-calendar-check"></i>
                <div class="status-details">
                  <h4>Time Elapsed</h4>
                  <p>8 months</p>
                </div>
              </div>
              <div class="status-item">
                <i class="fas fa-calendar-day"></i>
                <div class="status-details">
                  <h4>Time Remaining</h4>
                  <p>4 months</p>
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
              <h3>Planning</h3>
              <span class="phase-status completed">Completed</span>
            </div>
            <div class="phase-progress-bar">
              <div class="phase-progress-indicator" style="width: 100%;"></div>
            </div>
            <div class="phase-stats">
              <div class="phase-stat">
                <span>Start Date</span>
                <span>Jan 10, 2023</span>
              </div>
              <div class="phase-stat">
                <span>End Date</span>
                <span>Feb 28, 2023</span>
              </div>
              <div class="phase-stat">
                <span>Tasks</span>
                <span>8/8 Completed</span>
              </div>
            </div>
          </div>

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
                <span>Mar 1, 2023</span>
              </div>
              <div class="phase-stat">
                <span>End Date</span>
                <span>Apr 30, 2023</span>
              </div>
              <div class="phase-stat">
                <span>Tasks</span>
                <span>12/12 Completed</span>
              </div>
            </div>
          </div>

          <div class="phase-card">
            <div class="phase-header">
              <h3>Development</h3>
              <span class="phase-status in-progress">In Progress</span>
            </div>
            <div class="phase-progress-bar">
              <div class="phase-progress-indicator" style="width: 65%;"></div>
            </div>
            <div class="phase-stats">
              <div class="phase-stat">
                <span>Start Date</span>
                <span>May 1, 2023</span>
              </div>
              <div class="phase-stat">
                <span>End Date</span>
                <span>Oct, 2023</span>
              </div>
              <div class="phase-stat">
                <span>Tasks</span>
                <span>13/20 Completed</span>
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
                <span>Sep 1, 2023</span>
              </div>
              <div class="phase-stat">
                <span>End Date</span>
                <span>Nov 15, 2023</span>
              </div>
              <div class="phase-stat">
                <span>Tasks</span>
                <span>0/10 Completed</span>
              </div>
            </div>
          </div>

          <div class="phase-card">
            <div class="phase-header">
              <h3>Deployment</h3>
              <span class="phase-status upcoming">Upcoming</span>
            </div>
            <div class="phase-progress-bar">
              <div class="phase-progress-indicator" style="width: 0%;"></div>
            </div>
            <div class="phase-stats">
              <div class="phase-stat">
                <span>Start Date</span>
                <span>Nov 16, 2023</span>
              </div>
              <div class="phase-stat">
                <span>End Date</span>
                <span>Dec 15, 2023</span>
              </div>
              <div class="phase-stat">
                <span>Tasks</span>
                <span>0/5 Completed</span>
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
                <div class="slice slice1" style="--percentage: 40%; --color: var(--primary-color);"></div>
                <div class="slice slice2" style="--percentage: 25%; --color: #6c757d;"></div>
                <div class="slice slice3" style="--percentage: 20%; --color: #28a745;"></div>
                <div class="slice slice4" style="--percentage: 15%; --color: #17a2b8;"></div>
              </div>
              <div class="pie-legend">
                <div class="legend-item">
                  <span class="legend-color" style="background-color: var(--primary-color);"></span>
                  <span>Development (40%)</span>
                </div>
                <div class="legend-item">
                  <span class="legend-color" style="background-color: #6c757d;"></span>
                  <span>Design (25%)</span>
                </div>
                <div class="legend-item">
                  <span class="legend-color" style="background-color: #28a745;"></span>
                  <span>QA Testing (20%)</span>
                </div>
                <div class="legend-item">
                  <span class="legend-color" style="background-color: #17a2b8;"></span>
                  <span>Project Management (15%)</span>
                </div>
              </div>
            </div>
          </div>

          <div class="resource-card">
            <h3>Budget Allocation</h3>
            <div class="pie-chart-container">
              <div class="pie-chart">
                <div class="slice slice1" style="--percentage: 45%; --color: var(--primary-color);"></div>
                <div class="slice slice2" style="--percentage: 25%; --color: #6c757d;"></div>
                <div class="slice slice3" style="--percentage: 20%; --color: #28a745;"></div>
                <div class="slice slice4" style="--percentage: 10%; --color: #17a2b8;"></div>
              </div>
              <div class="pie-legend">
                <div class="legend-item">
                  <span class="legend-color" style="background-color: var(--primary-color);"></span>
                  <span>Development (45%)</span>
                </div>
                <div class="legend-item">
                  <span class="legend-color" style="background-color: #6c757d;"></span>
                  <span>Design (25%)</span>
                </div>
                <div class="legend-item">
                  <span class="legend-color" style="background-color: #28a745;"></span>
                  <span>Infrastructure (20%)</span>
                </div>
                <div class="legend-item">
                  <span class="legend-color" style="background-color: #17a2b8;"></span>
                  <span>Marketing (10%)</span>
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
          <p>Critical metrics tracking project health and success</p>
        </div>

        <div class="kpi-cards">
          <div class="kpi-card">
            <div class="kpi-icon">
              <i class="fas fa-tachometer-alt"></i>
            </div>
            <div class="kpi-content">
              <h3>Development Velocity</h3>
              <div class="kpi-value">
                <span>42</span>
                <span class="kpi-unit">Story Points/Sprint</span>
              </div>
              <div class="kpi-trend positive">
                <i class="fas fa-arrow-up"></i>
                <span>8% from last sprint</span>
              </div>
            </div>
          </div>

          <div class="kpi-card">
            <div class="kpi-icon">
              <i class="fas fa-bug"></i>
            </div>
            <div class="kpi-content">
              <h3>Defect Density</h3>
              <div class="kpi-value">
                <span>0.8</span>
                <span class="kpi-unit">Bugs/1000 LOC</span>
              </div>
              <div class="kpi-trend positive">
                <i class="fas fa-arrow-down"></i>
                <span>12% from last month</span>
              </div>
            </div>
          </div>

          <div class="kpi-card">
            <div class="kpi-icon">
              <i class="fas fa-code-branch"></i>
            </div>
            <div class="kpi-content">
              <h3>Code Coverage</h3>
              <div class="kpi-value">
                <span>87%</span>
              </div>
              <div class="kpi-trend positive">
                <i class="fas fa-arrow-up"></i>
                <span>5% from last release</span>
              </div>
            </div>
          </div>

          <div class="kpi-card">
            <div class="kpi-icon">
              <i class="fas fa-stopwatch"></i>
            </div>
            <div class="kpi-content">
              <h3>Cycle Time</h3>
              <div class="kpi-value">
                <span>4.2</span>
                <span class="kpi-unit">Days</span>
              </div>
              <div class="kpi-trend negative">
                <i class="fas fa-arrow-up"></i>
                <span>0.5 days increase</span>
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