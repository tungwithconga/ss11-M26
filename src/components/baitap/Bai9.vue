<template>
    <div>
      <h1>Ứng dụng đếm số</h1>
      <p>Count: {{ count }}</p>
      <p>Lần đầu component được render</p>
    </div>
  </template>
  
  <script setup>
  import { ref, onMounted, onUnmounted } from 'vue';
  
  const count = ref(0);
  let intervalId;
  
  onMounted(() => {
    intervalId = setInterval(() => {
      count.value++;
    }, 1000);
  });
  
  onUnmounted(() => {
    clearInterval(intervalId);
  });
  </script>
  