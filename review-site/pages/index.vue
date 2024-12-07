<template>
    <div class="home-container">
      <h1>Welcome to Our Review Site!</h1>
      <p>We provide honest and detailed reviews on movies, books, video games, and more.</p>
      <NuxtLink to="/reviews" class="cta-button">Explore Reviews</NuxtLink>
    </div>
  </template>
  
  <script setup>
  // No script needed for basic content
  </script>
  
  <style scoped>
  /* Pink theme styling */
  .home-container {
    max-width: 800px;
    margin: 20px auto;
    padding: 40px;
    background-color: #fce4ec;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    color: #6a1b9a;
    text-align: center;
  }
  
  h1 {
    color: #d81b60;
    font-family: 'Arial', sans-serif;
    font-size: 2rem;
  }
  
  p {
    font-size: 1.1rem;
    margin-bottom: 20px;
  }
  
  .cta-button {
    background-color: #ec407a;
    color: white;
    padding: 12px 20px;
    text-decoration: none;
    border-radius: 5px;
    font-size: 1.2rem;
  }
  
  .cta-button:hover {
    background-color: #d81b60;
  }
  </style>
  