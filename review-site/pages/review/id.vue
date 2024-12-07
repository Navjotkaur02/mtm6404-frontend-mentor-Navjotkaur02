<template>
    <div>
      <NuxtLink to="/">← Back to reviews</NuxtLink>
      <h1>{{ review?.title }}</h1>
      <p>{{ review?.content }}</p>
    </div>
  </template>
  
  <script setup>
  import { ref, onMounted } from 'vue';
  import { useRoute } from 'vue-router';
  import axios from 'axios';
  
  const route = useRoute();
  const review = ref(null);
  
  onMounted(async () => {
    const { data } = await axios.get(
      `${useRuntimeConfig().public.apiBase}/reviews/${route.params.id}`
    );
    review.value = data;
  });
  </script>
  
  <style scoped>
  h1 {
    margin-top: 20px;
  }
  </style>
  