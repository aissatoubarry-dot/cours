<script setup>
import { ref } from 'vue';

    const step = ref(1);
    const count = ref(0);

    function increment(){
        count.value += step.value;
    }

    function reset(){
        count.value = 0;
    }

</script>

<template>

   <div>

        <div>
            <button @click="increment">Increment (+)</button>
            <button @click="reset">Reset</button>
        </div>
        
        <div>
            <input type="number" min="1" v-model.number="step" @keyup.enter="increment">
        </div>

        <h4>{{ count }}</h4>

   </div>
  
</template>



<style scoped>

</style>