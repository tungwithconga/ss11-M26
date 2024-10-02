<template>
    <div>
      <h2>Child Component</h2>
      <p>Received Age: {{ age }}</p>
    </div>
  </template>
  
  <script setup>
  import { onUpdated, defineProps } from 'vue';
  
  const props = defineProps({
    age: Number
  });
  
  onUpdated(() => {
    alert('Giá trị của biến age đã thay đổi');
  });
  </script>
  