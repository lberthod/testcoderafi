<template>
  <div id="app">
    <header>
      <h1>Bois de Qualité à Grône, Valais</h1>
      <p>Le meilleur bois pour vos projets, directement du cœur du Valais.</p>
    </header>
    
    <HeroSection />
    <ServicesSection />
    <ContactSection />

    <footer>
      <p>&copy; 2024 Revendeur de Bois, Grône - Tous droits réservés.</p>
    </footer>
  </div>
</template>

<script setup>
import HeroSection from './components/HeroSection.vue'
import ServicesSection from './components/ServicesSection.vue'
import ContactSection from './components/ContactSection.vue'
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
}

header {
  background-color: #4CAF50;
  color: black;
  padding: 20px;
}

footer {
  background-color: #333;
  color: white;
  padding: 10px 0;
}
</style>
