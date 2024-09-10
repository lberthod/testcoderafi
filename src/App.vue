<template>
  <div id="app">
    <header class="app-header">
      <h1 class="header-title">Bois de Qualité à Grône, Valais</h1>
      <p class="header-subtitle">Le meilleur bois pour vos projets, directement du cœur du Valais.</p>
    </header>
    
    <HeroSection />
    <ServicesSection />
    <ContactSection />

    <footer class="app-footer">
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
/* Style global pour l'application */
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  text-align: center;
  color: #3e2c1c; /* Couleur marron foncé pour correspondre aux autres composants */
  background-color: #f5efe6; /* Beige clair pour le fond global */
  padding: 0;
  margin: 0;
}

/* Style pour l'en-tête */
.app-header {
  background-color: #8c5e34; /* Brun chaleureux en accord avec le thème bois */
  color: #f4f1ea; /* Couleur beige clair pour le texte */
  padding: 40px 20px;
  text-align: center;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.header-title {
  font-size: 2.5rem;
  margin-bottom: 10px;
}

.header-subtitle {
  font-size: 1.2rem;
  margin-top: 0;
  color: #d1b899; /* Couleur plus douce pour le sous-titre */
}

/* Style pour le pied de page */
.app-footer {
  background-color: #3e2c1c; /* Marron foncé pour correspondre au thème général */
  color: #f4f1ea; /* Couleur beige clair pour le texte */
  padding: 20px 0;
  text-align: center;
  box-shadow: 0 -4px 8px rgba(0, 0, 0, 0.1);
  margin-top: 40px;
}

.app-footer p {
  margin: 0;
  font-size: 0.9rem;
}

/* Responsive design pour les petits écrans */
@media (max-width: 768px) {
  .header-title {
    font-size: 2rem;
  }

  .header-subtitle {
    font-size: 1rem;
  }

  .app-footer {
    padding: 15px 0;
  }
}
</style>
