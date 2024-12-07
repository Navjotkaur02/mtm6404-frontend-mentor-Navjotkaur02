<template>
    <div class="contact-container">
      <h1>Contact Us</h1>
      <p>If you have any questions, feedback, or inquiries, please reach out to us!</p>
      
      <form @submit.prevent="submitForm">
        <div class="form-group">
          <label for="name">Name</label>
          <input id="name" v-model="formData.name" type="text" placeholder="Your Name" required />
        </div>
  
        <div class="form-group">
          <label for="email">Email</label>
          <input id="email" v-model="formData.email" type="email" placeholder="Your Email" required />
        </div>
  
        <div class="form-group">
          <label for="message">Message</label>
          <textarea id="message" v-model="formData.message" placeholder="Your Message" required></textarea>
        </div>
  
        <button type="submit">Submit</button>
      </form>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const formData = ref({
    name: '',
    email: '',
    message: '',
  });
  
  const submitForm = () => {
    alert(`Thank you, ${formData.value.name}! Your message has been sent.`);
    formData.value = { name: '', email: '', message: '' }; // Reset form
  };
  </script>
  
  <style scoped>
  /* Pink theme styling */
  .contact-container {
    max-width: 800px;
    margin: 20px auto;
    padding: 40px;
    background-color: #fce4ec;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    color: #6a1b9a;
  }
  
  h1 {
    color: #d81b60;
    font-family: 'Arial', sans-serif;
    text-align: center;
  }
  
  p {
    text-align: center;
    font-size: 1.2rem;
  }
  
  .form-group {
    margin-bottom: 20px;
  }
  
  label {
    display: block;
    margin-bottom: 8px;
  }
  
  input, textarea {
    width: 100%;
    padding: 12px;
    border: 1px solid #ec407a;
    border-radius: 5px;
    font-size: 1rem;
    color: #6a1b9a;
  }
  
  button {
    background-color: #ec407a;
    color: white;
    border: none;
    padding: 12px 20px;
    cursor: pointer;
    border-radius: 5px;
    font-size: 1.2rem;
    width: 100%;
    margin-top: 10px;
  }
  
  button:hover {
    background-color: #d81b60;
  }
  </style>
  