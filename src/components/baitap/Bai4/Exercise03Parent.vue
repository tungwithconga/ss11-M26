<template>
    <div>
      <h1>Parent Component</h1>
      <p>Age: {{ age }}</p>
      <button @click="increaseAge">Increase age</button>
      <Exercise03Children :age="age" />
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import Exercise03Children from './Exercise03Children.vue';
  
  const age = ref(1);
  
  const increaseAge = () => {
    age.value++;
  };
  </script>
  