<template>
  <div>
    <h1>ChildrenComponent</h1>
    <input type="text" v-model="inputValue">
    Count: {{count}}
  </div>
</template>

<script setup>
//Các phương thức trong giai đoạn khởi tạo creation
import { onBeforeMount,onMounted,onBeforeUpdate,onUpdated,ref } from 'vue';
const count = ref(0);
const inputValue = ref(0);

onBeforeMount(() => {
    count.value = 5;
  console.log('Component: beforeMount');
});
onMounted(() => {
    count.value = 6;
    console.log('Component: mounted');
});
//Các phương thức trong giai đoạn updation
onBeforeUpdate(() => {
    console.log('Component: beforeUpdate');
});
onUpdated(() => {
    console.log('Component: updated');
});
</script>

<style>

</style>