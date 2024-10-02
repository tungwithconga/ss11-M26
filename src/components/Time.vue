<template>
    <div>
      <h1>Time : {{ time }}</h1>
    </div>
  </template>
  
  <script setup>
  import {
    onBeforeMount,
    onBeforeUnmount,
    onBeforeUpdate,
    onMounted,
    onUnmounted,
    onUpdated,
  } from "vue";
  const time = ref(0);
  let timerId ;
  // giai doan mounting
  onBeforeMount(() => {
    console.log("components be fore mount");
  });
  onMounted(() => {
    console.log("components mounted");
    // setInterval(()=>{
    //     new Date().toLocaleTimeString()
    // },1000)
    timerId = setInterval(()=>{
        time.value++;
    },1000);
    console.log("components");
  });
  // giai doan updating
  onBeforeUpdate(() => {
    console.log("components be fore update");
  });
  onUpdated(() => {
    console.log("components updated");
  });
  // giai doan UnMount
  onBeforeUnmount(() => {
    console.log("components be fore unmount");
  });
  onUnmounted(() => {
    console.log("components unmounted");
  });
  </script>
  
  <style></style>