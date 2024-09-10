<template>
    <section class="hero">
        <img :src="logo" alt="Logo du revendeur de bois" class="hero-logo" />
        <h2>Bienvenue chez Bois Valais, votre fournisseur de bois local</h2>
      <p>Nous fournissons des matériaux de bois de haute qualité pour tous vos besoins de construction et de rénovation.</p>
    </section>
  </template>
  
  <script setup>
// Importation de l'image depuis assets
import logo from '../assets/logo.gif';
</script>

  <style scoped>
  .hero {
    padding: 50px 20px;
    background: url('/path/to/forest-image.jpg') no-repeat center center;
    background-size: cover;
    color: white;
  }
  
  .hero-logo {
    width: 150px;
    margin-bottom: 20px;
  }
  </style>
  