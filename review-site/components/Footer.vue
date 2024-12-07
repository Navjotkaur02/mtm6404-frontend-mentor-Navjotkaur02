<template>
    <footer class="footer">
      <div class="footer-container">
        <p>&copy; 2024 Review Site. All Rights Reserved.</p>
        <p>Follow us on:
          <a href="https://facebook.com" target="_blank">Facebook</a> |
          <a href="https://twitter.com" target="_blank">Twitter</a> |
          <a href="https://instagram.com" target="_blank">Instagram</a>
        </p>
      </div>
    </footer>
  </template>
  
  <script setup>
  // No script needed for basic footer content
  </script>
  
  <style scoped>
  /* Footer Styling */
  .footer {
    background-color: #ec407a;
    color: white;
    padding: 20px 0;
    text-align: center;
  }
  
  .footer-container {
    max-width: 1200px;
    margin: 0 auto;
  }
  
  .footer a {
    color: white;
    text-decoration: none;
  }
  
  .footer a:hover {
    text-decoration: underline;
  }
  </style>
  