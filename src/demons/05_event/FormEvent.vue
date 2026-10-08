
<script setup>
import { ref } from 'vue';


    const nom = ref("");
    const num = ref("");

    const contact = ref([]);

    function ajouter(){

        if (!nom.value.trim() || !num.value.trim() ) {

            return;
            
        }

        contact.value.unshift({

            id: crypto.randomUUID(),
            NomComplet: nom.value,
            Numero: num.value

        })

        nom.value = "";
        num.value = "";

    }

</script>

<template>

    <section>

        <form action="" @submit.prevent="ajouter">

            <input type="text" placeholder="NomComplet" v-model="nom">
            <input type="text" placeholder="Numero" v-model="num">

            <button type="submit">Ajouter</button>

        </form>

        {{ contact }}
        
    </section>
  
</template>


<style>

</style>