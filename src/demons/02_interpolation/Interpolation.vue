<script setup>

    const annee = new Date().getFullYear();
    const prime = 0.5;
    const salaire = 10000000000000000;

    const personne = {
        fullName: 'Aissatou',
        role: 'FullStack Dev'
    }

</script>


<template>

    <section class="card">
        <ul>
            <li>Nom: {{ personne.fullName }}</li>
            <li>Role: {{ personne.role }}</li>
            <li> Annee: {{ annee }}</li>
            <li> Salaire: {{ salaire.toLocaleString() }} £</li>
            <li> Salaire Net: {{ salaire + salaire*prime }} £</li>
        </ul>
    </section>
  
</template>


<style>

    .card{
        padding: 20px;

    }

    li{
        font-size: 20px;
        font-style: italic;
        color: #d46565;
    }

</style>