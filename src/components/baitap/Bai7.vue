<template>
    <div>
      <input type="text" v-model="inputValue" placeholder="Nhập tiêu đề..." />
    </div>
  </template>
  
  <script setup>
  import { ref, watch } from 'vue';
  
  const inputValue = ref('');
  
  watch(inputValue, (newValue) => {
    document.title = newValue;
  });
  </script>
  