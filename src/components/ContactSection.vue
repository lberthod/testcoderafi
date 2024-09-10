<template>
  <section class="contact">
    <h2 class="contact-title">Contactez-nous</h2>
    <form @submit.prevent="submitForm">
      <div class="form-group">
        <label for="name">Nom:</label>
        <input type="text" id="name" v-model="name" required />
      </div>
      <div class="form-group">
        <label for="email">Email:</label>
        <input type="email" id="email" v-model="email" required />
      </div>
      <div class="form-group">
        <label for="message">Message:</label>
        <textarea id="message" v-model="message" required></textarea>
      </div>
      <button type="submit" class="submit-button">Envoyer</button>
    </form>
  </section>
</template>

<script setup>
import { ref } from 'vue';

const name = ref('');
const email = ref('');
const message = ref('');

const submitForm = () => {
  console.log(`Nom: ${name.value}, Email: ${email.value}, Message: ${message.value}`);
  alert('Merci de nous avoir contactés!');
};
</script>

<style scoped>
/* Styles pour la section Contact */
.contact {
  padding: 60px 20px;
  background-color: #f4f1ea; /* Beige clair pour correspondre au thème bois */
  text-align: center;
}

.contact-title {
  font-size: 2.5rem;
  color: #3e2c1c; /* Marron foncé pour un aspect bois */
  margin-bottom: 40px;
}

/* Styles pour le formulaire */
form {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
  background-color: #ffffff;
  border: 1px solid #d1b899; /* Bordure beige douce pour un effet bois */
  border-radius: 12px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.form-group {
  width: 100%;
  margin-bottom: 20px;
  text-align: left;
}

label {
  font-size: 1rem;
  color: #3e2c1c; /* Couleur brun foncé pour les labels */
  margin-bottom: 5px;
  display: block;
}

input,
textarea {
  width: 100%;
  padding: 10px;
  border: 1px solid #d1b899;
  border-radius: 8px;
  font-size: 1rem;
  background-color: #f5efe6; /* Couleur douce pour l'intérieur des champs */
  color: #3e2c1c; /* Texte brun foncé */
  transition: border-color 0.3s ease, box-shadow 0.3s ease;
}

input:focus,
textarea:focus {
  border-color: #8c5e34; /* Changement de bordure au focus pour plus de visibilité */
  box-shadow: 0 0 5px rgba(140, 94, 52, 0.3);
  outline: none;
}

/* Styles pour le bouton */
.submit-button {
  padding: 12px 25px;
  background-color: #8c5e34; /* Brun chaleureux pour le bouton */
  color: #ffffff;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  font-size: 1rem;
  transition: background-color 0.3s ease;
}

.submit-button:hover {
  background-color: #5a3a20; /* Couleur plus foncée au survol */
}

/* Responsiveness */
@media (max-width: 768px) {
  .contact-title {
    font-size: 2rem;
  }

  form {
    padding: 15px;
  }

  input,
  textarea {
    font-size: 0.9rem;
  }
}
</style>
