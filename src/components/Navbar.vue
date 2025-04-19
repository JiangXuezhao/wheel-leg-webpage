<template>
  <header class="header" :class="{ 'sticky': isScrolled }">
    <div class="container">
      <nav class="navbar">
        <div class="logo">
          <router-link to="/">
            <span>Wheel-Leg</span>Robot
          </router-link>
        </div>
        <div class="menu-toggle" @click="toggleMenu">
          <i :class="isMenuOpen ? 'fas fa-times' : 'fas fa-bars'"></i>
        </div>
        <ul class="nav-links" :class="{ 'active': isMenuOpen }">
          <li><router-link to="/" @click="closeMenu">Home</router-link></li>
          <li><router-link to="/about" @click="closeMenu">About</router-link></li>
          <li><router-link to="/timeline" @click="closeMenu">Timeline</router-link></li>
          <li><router-link to="/statistics" @click="closeMenu">Statistics</router-link></li>
          <li><router-link to="/contact" @click="closeMenu">Contact</router-link></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Navbar',
  data() {
    return {
      isMenuOpen: false,
      isScrolled: false
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll)
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen
      document.body.classList.toggle('no-scroll', this.isMenuOpen)
    },
    closeMenu() {
      this.isMenuOpen = false
      document.body.classList.remove('no-scroll')
    },
    handleScroll() {
      this.isScrolled = window.scrollY > 50
    }
  }
}
</script>

<style scoped>
.header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  padding: 1.5rem 0;
  background-color: transparent;
  z-index: 1000;
  transition: var(--transition);
}

.header.sticky {
  padding: 1rem 0;
  background-color: rgba(255, 255, 255, 0.95);
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo a {
  font-size: 1.8rem;
  font-weight: 700;
  color: var(--dark-color);
}

.logo span {
  color: var(--primary-color);
  margin-right: 5px;
}

.nav-links {
  display: flex;
  list-style: none;
}

.nav-links li {
  margin-left: 2.5rem;
}

.nav-links a {
  font-weight: 500;
  color: var(--dark-color);
  position: relative;
}

.nav-links a:hover {
  color: var(--primary-color);
}

.nav-links a::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 0;
  height: 2px;
  background-color: var(--primary-color);
  transition: var(--transition);
}

.nav-links a:hover::after,
.nav-links a.router-link-active::after {
  width: 100%;
}

.menu-toggle {
  display: none;
  font-size: 1.5rem;
  cursor: pointer;
  color: var(--dark-color);
}

@media (max-width: 768px) {
  .menu-toggle {
    display: block;
  }

  .nav-links {
    position: fixed;
    top: 0;
    right: -100%;
    width: 250px;
    height: 100vh;
    background-color: white;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 2rem;
    box-shadow: -2px 0 10px rgba(0, 0, 0, 0.1);
    transition: right 0.3s ease;
  }

  .nav-links.active {
    right: 0;
  }

  .nav-links li {
    margin: 1.5rem 0;
  }
  
  body.no-scroll {
    overflow: hidden;
  }
}
</style> 