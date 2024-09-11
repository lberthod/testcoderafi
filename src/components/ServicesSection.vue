<template>
  <section class="services">
    <h2 class="services-title">Nos Services</h2>
    <div class="service-list">
      <div class="service" @mouseover="handleMouseOver" @mouseleave="handleMouseLeave">
        <div class="service-icon">
          <i class="fas fa-tree"></i>
        </div>
        <h3>Vente de Bois de chauffage</h3>
        <p>Le meilleur bois pour chauffer votre domicile</p>
      </div>
      <div class="service" @mouseover="handleMouseOver" @mouseleave="handleMouseLeave">
        <div class="service-icon">
          <i class="fas fa-truck"></i>
        </div>
        <h3>Livraison gratuite</h3>
        <p>Nous livrons gratuitement à partir de 3 stères dans toute la région du Valais.</p>
      </div>
      <div class="service" @mouseover="handleMouseOver" @mouseleave="handleMouseLeave">
        <div class="service-icon">
          <i class="fas fa-handshake"></i>
        </div>
        <h3>Conseil et Assistance</h3>
        <p>Nos experts sont à votre disposition pour vous aider à choisir le bon bois.</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  methods: {
    handleMouseOver(event) {
      event.currentTarget.style.transform = "scale(1.05)";
      event.currentTarget.style.boxShadow = "0 8px 16px rgba(0, 0, 0, 0.2)";
    },
    handleMouseLeave(event) {
      event.currentTarget.style.transform = "scale(1)";
      event.currentTarget.style.boxShadow = "0 4px 8px rgba(0, 0, 0, 0.1)";
    }
  }
};
</script>

<style scoped>
/* Styles généraux */
.services {
  padding: 60px 20px;
  background-color: #f4f1ea; /* Couleur de fond naturelle, proche du bois clair */
  text-align: center;
}

.services-title {
  font-size: 2.5rem;
  color: #3e2c1c; /* Marron foncé pour un aspect bois */
  margin-bottom: 40px;
}

/* Styles pour la liste des services */
.service-list {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 30px;
  padding: 0 10px;
}

/* Styles pour chaque service */
.service {
  width: 30%;
  min-width: 260px;
  padding: 25px;
  background-color: #ffffff;
  border: 1px solid #d1b899; /* Bordure beige douce pour un effet bois */
  border-radius: 12px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  text-align: left;
}

.service-icon {
  font-size: 2.5rem;
  margin-bottom: 15px;
  color: #8c5e34; /* Brun chaleureux pour les icônes */
}

.service h3 {
  color: #3e2c1c; /* Marron foncé pour les titres */
  margin-bottom: 10px;
}

.service p {
  color: #5a4b3f; /* Brun intermédiaire pour les textes */
  line-height: 1.6;
}

/* Effets d'interactivité */
.service:hover {
  cursor: pointer;
  background-color: #f5efe6; /* Couleur plus claire au survol pour un effet d'interaction douce */
  transform: scale(1.05);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.15);
}
</style>
