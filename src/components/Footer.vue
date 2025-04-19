<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-content">
        <div class="footer-logo">
          <h3><span>Wheel-Leg</span>Robot</h3>
          <p>A Parallel Balanced Wheel-Leg Robot Based on Deep Reinforcement Learning</p>
        </div>
        <div class="footer-links">
          <h4>Quick Links</h4>
          <ul>
            <li><router-link to="/">Home</router-link></li>
            <li><router-link to="/about">About</router-link></li>
            <li><router-link to="/timeline">Timeline</router-link></li>
            <li><router-link to="/statistics">Statistics</router-link></li>
            <li><router-link to="/contact">Contact</router-link></li>
          </ul>
        </div>
        <div class="footer-contact">
          <h4>Contact Us</h4>
          <p><i class="fas fa-envelope"></i> u3638184@connect.hku.hk</p>
          <p><i class="fas fa-phone"></i> Faculty of Engineering, HKU</p>
          <p><i class="fas fa-map-marker-alt"></i> The University of Hong Kong</p>
        </div>
        <div class="footer-social">
          <h4>Follow Us</h4>
          <div class="social-icons">
            <a href="#" aria-label="GitHub"><i class="fab fa-github"></i></a>
            <a href="#" aria-label="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
            <a href="#" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
          </div>
        </div>
      </div>
      <div class="footer-bottom">
        <p>&copy; {{ new Date().getFullYear() }} Wheel-Leg Robot Project. All Rights Reserved.</p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style scoped>
.footer {
  background-color: var(--dark-color);
  color: white;
  padding: 5rem 0 1rem;
}

.footer-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 2rem;
  margin-bottom: 3rem;
}

.footer-logo h3 {
  font-size: 1.8rem;
  font-weight: 700;
  margin-bottom: 1rem;
}

.footer-logo span {
  color: var(--primary-color);
  margin-right: 5px;
}

.footer-logo p {
  color: rgba(255, 255, 255, 0.7);
  margin-bottom: 1.5rem;
}

.footer h4 {
  font-size: 1.2rem;
  margin-bottom: 1.5rem;
  position: relative;
}

.footer h4::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: -10px;
  width: 50px;
  height: 3px;
  background-color: var(--primary-color);
}

.footer-links ul {
  list-style: none;
}

.footer-links li {
  margin-bottom: 0.8rem;
}

.footer-links a {
  color: rgba(255, 255, 255, 0.7);
}

.footer-links a:hover {
  color: var(--primary-color);
}

.footer-contact p {
  display: flex;
  align-items: center;
  color: rgba(255, 255, 255, 0.7);
  margin-bottom: 1rem;
}

.footer-contact p i {
  margin-right: 10px;
  color: var(--primary-color);
}

.social-icons {
  display: flex;
  gap: 10px;
}

.social-icons a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background-color: rgba(255, 255, 255, 0.1);
  color: white;
  transition: var(--transition);
}

.social-icons a:hover {
  background-color: var(--primary-color);
  transform: translateY(-3px);
}

.footer-bottom {
  text-align: center;
  padding-top: 2rem;
  border-top: 1px solid rgba(255, 255, 255, 0.1);
}

.footer-bottom p {
  color: rgba(255, 255, 255, 0.7);
  font-size: 0.9rem;
}

@media (max-width: 768px) {
  .footer-content {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .footer-content {
    grid-template-columns: 1fr;
  }
}
</style> 