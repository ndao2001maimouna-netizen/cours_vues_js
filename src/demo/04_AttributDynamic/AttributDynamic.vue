<script setup>
import { ref } from 'vue';
const status = ref('warning')

</script>

<template>
    <section class="card">
     <h1>04_Dynamic Attribut</h1>
        
     <div class="row">
        <span>Status: {{ status }}</span>
            <select v-model="status">
                <option value="success">Success</option>
                <option value="warning">Warning</option>
                <option value="danger">Danger</option>
            </select>
            <input type="text" v-model="inputField">
            <p>{{ status }}</p>
            <h1>{{ inputField }}</h1>
     </div>
     <div class="bar" :style= "{ width:status ==='danger' ? '20%': status==='warning' ? '50%' : '80%'}"></div>

    </section>
  
</template>


<style scoped>
     .card{
    padding: 16px;
    border: 1px solid #eee;
    border-radius: 12px;
  }
    .row{
        display: flex;
        gap: 12px;
        align-items: centre;
    }
    .badge{
        padding: 6px 10px;
        border-radius: 999px;
        font-weight: 600;
        border: 1px solid #ddd;
    }

    .success{background: #e9f7ef;}
    .warning{background: #fff7e6;}
    .danger{background: #fdecea;}

    .bar{
        height: 10px;
        border-radius: 999px;
        border: 1px solid #eee;
        background: #ddd;
        margin-top: 14px;
    }

    select{
        padding: 8px 10px;
        border: 1px solid #ddd;
        border-radius: 8px;
    }
    
</style>