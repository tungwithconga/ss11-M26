<template>
    <div>
      <h1>Current Company: {{ currentCompany }}</h1>
      <p>Age: {{ age }}</p>
      <button @click="randomizeAge">Random</button>
    </div>
  </template>
  
  <script setup>
  import { ref, computed } from 'vue';
  
  const age = ref(1);
  
  const companies = ["Rikkei Academy", "Rikkei Education", "Rikkei Fukuoka"];
  
  const randomizeAge = () => {
    age.value = Math.floor(Math.random() * 10) + 1;
  };
  
  const currentCompany = computed(() => {
    return companies[age.value % companies.length];
  });
  </script>
  
  