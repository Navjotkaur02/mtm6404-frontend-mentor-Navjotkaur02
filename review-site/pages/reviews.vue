<template>
    <div class="reviews-container">
      <h1>Reviews</h1>
  
      <!-- Add Review Form -->
      <div class="add-review-form">
        <h2>Add a Review</h2>
        <form @submit.prevent="addReview">
          <div class="form-group">
            <label for="name">Name</label>
            <input
              v-model="newReview.name"
              type="text"
              id="name"
              placeholder="Enter your name"
              required
            />
          </div>
          
          <div class="form-group">
            <label for="email">Email</label>
            <input
              v-model="newReview.email"
              type="email"
              id="email"
              placeholder="Enter your email"
              required
            />
          </div>
          
          <div class="form-group">
            <label for="description">Description</label>
            <textarea
              v-model="newReview.description"
              id="description"
              placeholder="Enter your review"
              required
            ></textarea>
          </div>
  
          <button type="submit">Add Review</button>
        </form>
      </div>
  
      <!-- Display Reviews -->
      <div class="reviews-list">
        <h2>All Reviews</h2>
        <div v-if="reviews.length === 0">
          <p>No reviews yet. Be the first to add a review!</p>
        </div>
        <div v-for="(review, index) in reviews" :key="index" class="review-item">
          <h3>{{ review.name }}</h3>
          <p><strong>Email:</strong> {{ review.email }}</p>
          <p><strong>Review:</strong> {{ review.description }}</p>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const reviews = ref([]); // Array to hold reviews
  const newReview = ref({
    name: '',
    email: '',
    description: ''
  });
  
  // Function to add a new review
  const addReview = () => {
    if (newReview.value.name && newReview.value.email && newReview.value.description) {
      reviews.value.push({ ...newReview.value });  // Add new review to the list
      // Reset the form fields
      newReview.value = { name: '', email: '', description: '' };
    } else {
      alert('Please fill in all fields');
    }
  };
  </script>
  
  <style scoped>
  /* Styling for Reviews Page */
  .reviews-container {
    max-width: 900px;
    margin: 20px auto;
    padding: 40px;
    background-color: #fce4ec;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    color: #6a1b9a;
  }
  
  h1 {
    color: #d81b60;
    text-align: center;
    font-size: 2rem;
  }
  
  h2 {
    color: #d81b60;
    font-size: 1.5rem;
  }
  
  .add-review-form {
    background-color: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
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
  
  .reviews-list {
    margin-top: 40px;
  }
  
  .review-item {
    background-color: white;
    padding: 20px;
    margin-bottom: 20px;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }
  
  .review-item h3 {
    color: #d81b60;
  }
  
  .review-item p {
    color: #6a1b9a;
  }
  </style>
  