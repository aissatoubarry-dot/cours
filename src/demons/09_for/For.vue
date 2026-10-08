<script setup>

import { reactive, ref } from 'vue';

const products = ref([
    {id:1,nom:'bic', prix:4000, stock:10},
    {id:2,nom:'cahier', prix:2222, stock:4},
    {id:3,nom:'livre', prix:2000, stock:9},
    {id:4,nom:'crayon', prix:10000, stock:1}
]);

const supprimer = (id)=>{ 
    products.value = products.value.filter((p)=>p.id != id)
 }
</script>

<template>
  <section class="card">
    <h2>13 - Lists</h2>

    <ul>
      <li v-for="p in products" :key="p.id">
        {{p.nom}} - {{p.prix}} FCFA
        <button @click="supprimer(p.id)">❌</button>
      </li>
    </ul>
  </section> 
</template>

<style scoped>
.card { padding:16px; border:1px solid #eee; border-radius:12px; }
li { display:flex; justify-content:space-between; width:250px; }
button { border:none; background:none; cursor:pointer; }
</style>