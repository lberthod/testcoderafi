<template>
    <section class="contact">
      <h2>Contactez-nous</h2>
      <form @submit.prevent="submitForm">
        <div>
          <label for="name">Nom:</label>
          <input type="text" id="name" v-model="name" required />
        </div>
        <div>
          <label for="email">Email:</label>
          <input type="email" id="email" v-model="email" required />
        </div>
        <div>
          <label for="message">Message:</label>
          <textarea id="message" v-model="message" required></textarea>
        </div>
        <button type="submit">Envoyer</button>
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
  .contact {
    padding: 50px 20px;
    background-color: #eeeeee;
  }
  
  form {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    max-width: 600px;
    margin: 0 auto;
  }
  
  form div {
    margin-bottom: 20px;
  }
  
  button {
    padding: 10px 20px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  </style>
  