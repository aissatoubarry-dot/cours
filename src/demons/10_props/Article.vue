<script setup>

// defineProps({
//     barry:Object,
//     quantite:Number
// });

const propriete = defineProps({
    barry:{
        type:Object,
        required:true,
        validator:(value)=>{
            return value && typeof value.name === "string";
        }
    },
    quantite:Number,
    status: {
        type:Boolean,
        required:true
    }
});

console.log(propriete.barry);

</script>

<template>

    <article class="card">
        <h3 class="name">{{ barry.name }}</h3>
        <p class="price">{{ barry.price.toLocaleString() }} FCFA</p>
        <p class="meta">ID: {{ barry.id }}</p>
        <p class="meta">Quantité: {{ quantite }}</p>
    </article>

</template>

<style scoped>

.card { padding: 14px; border: 1px solid #eee; border-radius: 12px; background: #fff; }
.name { margin: 0; font-size: 16px; }
.price { margin: 6px 0 0; font-weight: 700; }
.meta { margin: 6px 0 0; color: #666; font-size: 12px; }

</style>