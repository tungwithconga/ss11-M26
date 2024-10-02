<template>
  <div>
    <h1>Count: {{ count }}</h1>
    <button @click="increment">Counter</button>
  </div>
</template>

<script setup>
import { ref, onUpdated } from 'vue';

const count = ref(0);

const increment = () => {
  count.value++;
};

onUpdated(() => {
  console.log('Dữ liệu đã thay đổi');
});
</script>
