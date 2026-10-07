<script setup>

    const image = "https://i.pinimg.com/1200x/1e/56/db/1e56db3cfd9a98604d1e3de9828ef93d.jpg";
    const btn = false;

</script>

<template>

    <!-- <img v-bind=" image " alt="ma photo"> -->
    <img :src=" image " alt="ma photo">

    <button :disabled = "btn"> Click me </button>

  
</template>



<style>

    img{
        width: 50%;
    }

</style>