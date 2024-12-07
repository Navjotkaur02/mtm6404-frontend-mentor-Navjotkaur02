<template>
    <nav class="navbar">
      <div class="navbar-container">
        <NuxtLink to="/" class="navbar-logo">Home</NuxtLink>
        <div class="navbar-links">
          <NuxtLink to="/reviews" class="navbar-link">Reviews</NuxtLink>
          <NuxtLink to="/contact" class="navbar-link">Contact Us</NuxtLink>
        </div>
      </div>
    </nav>
  </template>
  
  <script setup>
  // No script needed for basic content
  </script>
  
  <style scoped>
  /* Navigation Bar Styling */
  .navbar {
    background-color: #ec407a;  /* Pink background */
    padding: 10px 0;
    position: sticky;
    top: 0;
    z-index: 1000;
    display: flex;
    justify-content: center;  /* Center the navbar content */
  }
  
  .navbar-container {
    max-width: 1200px;
    display: flex;
    justify-content: center;  /* Center content inside navbar-container */
    align-items: center;
    width: 100%;
  }
  
  .navbar-logo {
    font-size: 1.2rem;  /* Same font size as the navbar links */
    color: white;
    text-decoration: none;
    font-weight: bold;
    margin-right: 40px;  /* Add some space between the logo and the links */
  }
  
  .navbar-links {
    display: flex;
    gap: 30px;  /* Add some space between the navigation links */
  }
  
  .navbar-link {
    font-size: 1.2rem;  /* Set font size of the links */
    color: white;
    text-decoration: none;
  }
  
  .navbar-link:hover {
    text-decoration: underline;
  }
  </style>
  