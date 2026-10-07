
<script setup>

    import { ref } from 'vue';

    const status = ref("warning");

</script>

<template>

    <section class="card">

        <h2>04_Dynamic Attribut</h2>

        <div class="row">
            <span>Statut</span>
            <select v-model="status"> 
                <option value="success">Success</option>
                <option value="warning">Warning</option>
                <option value="danger">Danger</option>
            </select>
            <p>{{ status }}</p>
        </div>

        <div class="bar" :style="{width:'50%'}"></div>

    </section>
  
</template>


<style scoped>

.card{
  background-color: rgb(212, 235, 227);
  padding: 16px;
  border: 1px solid #eee;
  border-radius: 12px;
}

.row{
    display: flex;
    gap: 12px;
    align-items: center;
}

.badge{
    padding: 6px 10px ;
    border-radius: 999px;
    font-weight: 600;
    border: 1px solid #ddd;
}

.success{ background-color: #e9f7ef; }
.warning{ background-color: #fff7ef; }
.danger{ background-color: #fdecea; }
.bar{ 
    height: 10px;
    border-radius: 990px;
    border: 1px solid #eee;
    background-color: #ddd;
    margin-top: 14px;
}

select{
    padding: 8px 10px;
    border: 1px solid #ddd;
    border-radius: 8px;
}



</style>