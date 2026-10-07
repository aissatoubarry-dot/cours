<script setup>

const message = "Shine bright like a diamond";

</script>


<template>

  <section class="card">
      <h2> 01_Hello_BARRYYYYYWORLD</h2>
      <p>Premier composant vue (SFC)</p>
      <div class="box">
            <strong>Message:</strong>{{ message.toUpperCase() }}
      </div>
  </section>
  
</template>



<style>

.card{
  background-color: rgb(212, 235, 227);
  padding: 16px;
  border: 1px solid #eee;
  border-radius: 12px;
}

.box{
  margin-top: 10px;
  padding: 12px;
  border: 1px dashed #d46565;
  border-radius: 10px;
}

</style>