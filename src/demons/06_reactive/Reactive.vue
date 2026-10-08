<script setup>
import { reactive, ref } from 'vue';


const personne = reactive ({
    nom: "Aissatou",
    tel: 7888999999,
    solde: 10000000000000000
})

const autre = ref();

const count = ref(0);

function augmenter(montant){

    if (count.value < 10) {

        personne.solde+=montant;
        count.value++;

    }

    autre.value=0;
    return;

}


</script>

<template>
  <section class="card">
    <h2>09 - reactive()</h2>

    <div class="box">
      <p><strong>Nom :</strong> {{ personne.nom }} </p>
      <p><strong>Téléphone :</strong> {{ personne.tel }} </p>
      <p><strong>Solde :</strong> {{ personne.solde }} FCFA</p>
      <p><strong>Count Ajout:</strong>{{ count }}</p>
    </div>

    <div class="actions">
      <button @click="augmenter(5000)">+5 000</button>
      <button @click="augmenter(10000)">+10 000</button>
      <input type="number" placeholder="Autre montant" v-model="autre" @keyup.enter="augmenter(autre)">
    </div>

    <p class="note">
      <code>reactive()</code> est idéal pour les objets complexes.
    </p>
  </section>
</template>

<style scoped>
.card { padding:16px; border:1px solid #eee; border-radius:12px; }
.box { padding:12px; background:#fafafa; border-radius:10px; }
.actions { display:flex; gap:10px; margin-top:10px; }
button { padding:8px 10px; border:1px solid #ddd; border-radius:8px; }
.note { margin-top:8px; color:#555; }
</style>