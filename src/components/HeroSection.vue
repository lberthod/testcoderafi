<template>
  <section class="hero">
    <img :src="logo" alt="Logo du revendeur de bois" class="hero-logo" />
    <h2 class="hero-title">Bienvenue chez Serafim Bois, votre fournisseur de bois local</h2>
    <h2 class="hero-subtitle">Une qualité inimaginable</h2>
    <p class="hero-description">Nous vous fournissons du bois de haute qualité pour chauffer votre domicile.</p>
  </section>
</template>

<script setup>
// Importation de l'image depuis les assets
import logo from '../assets/logo.png';
</script>

<style scoped>
/* Styles généraux pour la section Hero */
.hero {
  padding: 60px 20px;
  background: url('/path/to/forest-image.jpg') no-repeat center center;
  background-size: cover;
  color: #ffffff; /* Texte blanc pour contraste avec l'image de fond */
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 60vh;
  background-blend-mode: overlay; /* Mélange des couleurs pour un effet doux */
  background-color: rgba(62, 44, 28, 0.7); /* Overlay avec une teinte boisée */
}

.hero-logo {
  width: 150px;
  margin-bottom: 20px;
  border-radius: 8px; /* Arrondir légèrement les coins pour correspondre au style précédent */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Ombre pour donner de la profondeur */
  transition: transform 0.3s ease;
}

.hero-title {
  font-size: 2.5rem;
  color: #f4f1ea; /* Utilisation du beige clair pour correspondre à l'autre section */
  margin-bottom: 10px;
  font-weight: 700;
}

.hero-subtitle {
  font-size: 1.8rem;
  color: #d1b899; /* Teinte beige douce pour s'harmoniser avec la palette de couleurs */
  margin-bottom: 20px;
}

.hero-description {
  font-size: 1.2rem;
  line-height: 1.6;
  max-width: 600px;
  color: #f5efe6; /* Texte légèrement plus clair pour une meilleure lisibilité */
  margin-bottom: 30px;
}

/* Effets d'interactivité */
.hero-logo:hover {
  transform: scale(1.1);
  cursor: pointer;
}

@media (max-width: 768px) {
  .hero {
    padding: 40px 10px;
  }

  .hero-title {
    font-size: 2rem;
  }

  .hero-subtitle {
    font-size: 1.5rem;
  }

  .hero-description {
    font-size: 1rem;
  }
}
</style>
