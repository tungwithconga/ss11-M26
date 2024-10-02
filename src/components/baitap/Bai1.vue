<template>
  <div>
    <h1>onMounted</h1>
  </div>
</template>

<script setup>
import { onMounted} from 'vue';

onMounted(() => {
console.log("Component onMounted")
});

</script>

<style>

</style>