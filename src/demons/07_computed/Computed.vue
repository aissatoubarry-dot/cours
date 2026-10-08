<script setup>
import { reactive } from 'vue';


const cart = reactive([
    {nom:'cahier', prix:2222, stock:4},
    {nom:'bic', prix:4000, stock:10},
    {nom:'livre', prix:2000, stock:9},
    {nom:'crayon', prix:10000, stock:1}
])

</script>

<template>
  <section class="card">
    <h2>11 - computed()</h2>

    <ul>
      <li v-for="item in cart" :key="item.name">
       ... × ... -> ... FCFA
      </li>
    </ul>

    <h3>Total : ... FCFA</h3>

    <p class="note">
      Le total se met à jour automatiquement.
    </p>
  </section>
</template>

<style scoped>
.card { padding:16px; border:1px solid #eee; border-radius:12px; }
.note { margin-top:8px; color:#555; }
</style>