<template>
    <div>
      <h1>Parent Component</h1>
      <button @click="toggleChild">Toggle</button>
      
      <Exercise05Children v-if="isChildVisible" />
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import Exercise05Children from './Exercise05Children.vue';
  
  const isChildVisible = ref(true);
  
  const toggleChild = () => {
    isChildVisible.value = !isChildVisible.value;
  };
  </script>
  