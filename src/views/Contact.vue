<template>
  <div class="contact-page">
    <!-- Page Header -->
    <section class="page-header">
      <div class="container">
        <h1>Contact Us</h1>
        <p>Get in touch with our team for more information about the wheel-leg robot project</p>
      </div>
    </section>

    <!-- Contact Form Section -->
    <section class="section form-section">
      <div class="container">
        <div class="contact-container">
          <div class="contact-info">
            <div class="section-title text-left">
              <h2>Get In Touch</h2>
              <p>We'd love to hear from you. Here's how you can reach our team.</p>
            </div>

            <div class="info-items">
              <div class="info-item">
                <div class="info-icon">
                  <i class="fas fa-map-marker-alt"></i>
                </div>
                <div class="info-content">
                  <h3>Our Location</h3>
                  <p>Faculty of Engineering, The University of Hong Kong</p>
                </div>
              </div>

              <div class="info-item">
                <div class="info-icon">
                  <i class="fas fa-envelope"></i>
                </div>
                <div class="info-content">
                  <h3>Email Us</h3>
                  <p>u3638184@connect.hku.hk</p>
                  <p>loretta.choi@hku.hk (Project Mentor)</p>
                </div>
              </div>

              <div class="info-item">
                <div class="info-icon">
                  <i class="fas fa-user"></i>
                </div>
                <div class="info-content">
                  <h3>Project Team</h3>
                  <p>Jiang Xuezhao, Wu Teng, Wu Jiatong, Wen Hao</p>
                  <p>Mentor: Dr. Loretta Y.K. Choi</p>
                </div>
              </div>

              <div class="info-item">
                <div class="info-icon">
                  <i class="fas fa-clock"></i>
                </div>
                <div class="info-content">
                  <h3>Research Period</h3>
                  <p>April 2025 - July 2025</p>
                </div>
              </div>
            </div>

            <div class="social-links">
              <h3>Project Resources</h3>
              <div class="social-icons">
                <a href="#" aria-label="GitHub"><i class="fab fa-github"></i></a>
                <a href="#" aria-label="Research Paper"><i class="fas fa-file-alt"></i></a>
                <a href="#" aria-label="Video Demo"><i class="fab fa-youtube"></i></a>
              </div>
            </div>
          </div>

          <div class="contact-form">
            <div class="section-title text-left">
              <h2>Send a Message</h2>
              <p>Fill out the form below if you have questions about our wheel-leg robot research.</p>
            </div>

            <form @submit.prevent="submitForm">
              <div class="form-group">
                <label for="name">Your Name</label>
                <input 
                  type="text" 
                  id="name" 
                  v-model="form.name" 
                  placeholder="Enter your full name"
                  required
                />
              </div>

              <div class="form-group">
                <label for="email">Email Address</label>
                <input 
                  type="email" 
                  id="email" 
                  v-model="form.email" 
                  placeholder="Enter your email address"
                  required
                />
              </div>

              <div class="form-group">
                <label for="subject">Subject</label>
                <input 
                  type="text" 
                  id="subject" 
                  v-model="form.subject" 
                  placeholder="Enter message subject"
                  required
                />
              </div>

              <div class="form-group">
                <label for="message">Your Message</label>
                <textarea 
                  id="message" 
                  v-model="form.message" 
                  rows="6" 
                  placeholder="Enter your message"
                  required
                ></textarea>
              </div>

              <button type="submit" class="btn btn-block">Send Message</button>
            </form>

            <div v-if="formStatus.submitted" class="form-submitted">
              <div :class="['status-message', formStatus.success ? 'success' : 'error']">
                <i :class="formStatus.success ? 'fas fa-check-circle' : 'fas fa-exclamation-circle'"></i>
                <p>{{ formStatus.message }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Map Section -->
    <section class="section map-section">
      <div class="map-container">
        <iframe 
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3691.9194365051975!2d114.1362445761142!3d22.283030079823597!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3403ff20b7f6f2ad%3A0xccdee9f7fe6f8ef9!2sHong%20Kong%20University!5e0!3m2!1sen!2sus!4v1682341829271!5m2!1sen!2sus" 
          width="100%" 
          height="450" 
          style="border:0;" 
          allowfullscreen="" 
          loading="lazy" 
          referrerpolicy="no-referrer-when-downgrade"
        ></iframe>
      </div>
    </section>

    <!-- FAQ Section -->
    <section class="section faq-section">
      <div class="container">
        <div class="section-title">
          <h2>Frequently Asked Questions</h2>
          <p>Find answers to common questions about our wheel-leg robot project</p>
        </div>

        <div class="faq-container">
          <div class="faq-item" v-for="(faq, index) in faqs" :key="index">
            <div 
              class="faq-question" 
              :class="{ 'active': faq.isOpen }"
              @click="toggleFaq(index)"
            >
              <h3>{{ faq.question }}</h3>
              <i :class="faq.isOpen ? 'fas fa-minus' : 'fas fa-plus'"></i>
            </div>
            <div class="faq-answer" :class="{ 'active': faq.isOpen }">
              <p>{{ faq.answer }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'Contact',
  data() {
    return {
      form: {
        name: '',
        email: '',
        subject: '',
        message: ''
      },
      formStatus: {
        submitted: false,
        success: false,
        message: ''
      },
      faqs: [
        {
          question: 'What is a wheel-leg robot?',
          answer: 'Wheel-legged robots are a new type of robot that combines the characteristics of wheeled and legged robots. They are able to move flexibly over different terrains through the combination of wheels and legs, and are more adaptable in complex environments than traditional wheeled robots.',
          isOpen: true
        },
        {
          question: 'What technologies are being used in this project?',
          answer: 'Our project employs Deep Reinforcement Learning (DRL), specifically using algorithms like DQN (Deep Q Network) and PPO (Proximal Policy Optimization). We also use ROS (Robot Operating System), SolidWorks for mechanical modeling, and simulation platforms like Wheel-Legged-Gym.',
          isOpen: false
        },
        {
          question: 'What are the main benefits of wheel-leg robots?',
          answer: 'Wheel-leg robots combine the efficiency of wheels with the versatility of legs, allowing them to navigate complex terrains that would be challenging for traditional wheeled robots. They can maintain stability on uneven surfaces, climb obstacles, and adapt to various environmental conditions.',
          isOpen: false
        },
        {
          question: 'How does Deep Reinforcement Learning improve robot movement?',
          answer: 'DRL enables the robot to learn optimal movement strategies through trial-and-error interactions with its environment. By receiving rewards for successful actions and penalties for failures, the robot learns to navigate complex terrains efficiently without requiring explicit programming for every possible scenario.',
          isOpen: false
        },
        {
          question: 'What are the real-world applications for this research?',
          answer: 'Wheel-leg robots have potential applications in disaster response, exploration of hazardous or inaccessible environments, planetary exploration, industrial inspection, agricultural operations, and any scenario requiring mobility over challenging terrains where traditional robots might struggle.',
          isOpen: false
        }
      ]
    }
  },
  methods: {
    submitForm() {
      // Simulate form submission
      this.formStatus.submitted = true
      
      // Simulate successful submission (in a real application, this would be an API call)
      setTimeout(() => {
        this.formStatus.success = true
        this.formStatus.message = 'Your message has been sent successfully! We will get back to you soon.'
        
        // Reset form after successful submission
        this.form = {
          name: '',
          email: '',
          subject: '',
          message: ''
        }
      }, 1500)
    },
    toggleFaq(index) {
      this.faqs.forEach((faq, i) => {
        if (i === index) {
          faq.isOpen = !faq.isOpen
        } else {
          faq.isOpen = false
        }
      })
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

/* Form Section */
.form-section {
  padding-bottom: 0;
}

.contact-container {
  display: grid;
  grid-template-columns: 1fr 1.3fr;
  gap: 4rem;
}

.text-left {
  text-align: left;
}

.text-left h2::after {
  left: 0;
  transform: none;
}

.text-left p {
  margin: 0 0 2rem;
}

/* Contact Info */
.info-items {
  margin-bottom: 2.5rem;
}

.info-item {
  display: flex;
  margin-bottom: 2rem;
}

.info-icon {
  flex-shrink: 0;
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

.info-content h3 {
  font-size: 1.3rem;
  margin-bottom: 0.5rem;
  color: var(--dark-color);
}

.info-content p {
  color: var(--secondary-color);
  margin-bottom: 0.3rem;
}

.social-links h3 {
  font-size: 1.3rem;
  margin-bottom: 1.5rem;
  color: var(--dark-color);
}

.social-icons {
  display: flex;
  gap: 1rem;
}

.social-icons a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background-color: rgba(74, 108, 247, 0.1);
  color: var(--primary-color);
  transition: var(--transition);
}

.social-icons a:hover {
  background-color: var(--primary-color);
  color: white;
  transform: translateY(-3px);
}

/* Contact Form */
.contact-form {
  background-color: white;
  padding: 3rem;
  border-radius: var(--border-radius);
  box-shadow: 0 5px 30px rgba(0, 0, 0, 0.08);
}

.form-group {
  margin-bottom: 1.5rem;
}

.form-group label {
  display: block;
  margin-bottom: 0.5rem;
  font-weight: 500;
  color: var(--dark-color);
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 0.8rem 1rem;
  border: 1px solid var(--border-color);
  border-radius: 5px;
  background-color: #f8f9fa;
  transition: var(--transition);
}

.form-group input:focus,
.form-group textarea:focus {
  outline: none;
  border-color: var(--primary-color);
  box-shadow: 0 0 0 3px rgba(74, 108, 247, 0.1);
}

.btn-block {
  width: 100%;
  margin-top: 1rem;
}

.form-submitted {
  margin-top: 2rem;
}

.status-message {
  display: flex;
  align-items: center;
  padding: 1rem;
  border-radius: 5px;
}

.status-message.success {
  background-color: rgba(40, 167, 69, 0.1);
  color: var(--success-color);
}

.status-message.error {
  background-color: rgba(220, 53, 69, 0.1);
  color: var(--danger-color);
}

.status-message i {
  font-size: 1.5rem;
  margin-right: 1rem;
}

.status-message p {
  margin: 0;
}

/* Map Section */
.map-section {
  padding: 0;
}

.map-container {
  margin-top: 5rem;
  height: 450px;
  width: 100%;
}

.map-container iframe {
  display: block;
}

/* FAQ Section */
.faq-section {
  background-color: var(--light-color);
}

.faq-container {
  max-width: 800px;
  margin: 0 auto;
}

.faq-item {
  margin-bottom: 1.5rem;
  background-color: white;
  border-radius: var(--border-radius);
  overflow: hidden;
  box-shadow: 0 3px 10px rgba(0, 0, 0, 0.05);
}

.faq-question {
  padding: 1.5rem;
  cursor: pointer;
  display: flex;
  justify-content: space-between;
  align-items: center;
  transition: var(--transition);
}

.faq-question:hover {
  background-color: rgba(0, 0, 0, 0.01);
}

.faq-question.active {
  border-bottom: 1px solid var(--border-color);
}

.faq-question h3 {
  font-size: 1.1rem;
  margin: 0;
  color: var(--dark-color);
}

.faq-question i {
  color: var(--primary-color);
  font-size: 1rem;
}

.faq-answer {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.3s ease;
}

.faq-answer.active {
  max-height: 500px;
}

.faq-answer p {
  padding: 1.5rem;
  margin: 0;
  color: var(--secondary-color);
  line-height: 1.7;
}

/* Responsive Styles */
@media (max-width: 992px) {
  .page-header h1 {
    font-size: 2.5rem;
  }
  
  .contact-container {
    grid-template-columns: 1fr;
    gap: 3rem;
  }
  
  .contact-info {
    order: 2;
  }
  
  .contact-form {
    order: 1;
  }
}

@media (max-width: 768px) {
  .info-item {
    flex-direction: column;
  }
  
  .info-icon {
    margin-right: 0;
    margin-bottom: 1rem;
  }
  
  .contact-form {
    padding: 2rem;
  }
  
  .faq-question h3 {
    font-size: 1rem;
  }
}

@media (max-width: 576px) {
  .page-header {
    padding: 6rem 0 3rem;
  }
  
  .page-header h1 {
    font-size: 2rem;
  }
  
  .form-section {
    padding-top: 3rem;
  }
  
  .map-container {
    margin-top: 3rem;
    height: 350px;
  }
}
</style> 