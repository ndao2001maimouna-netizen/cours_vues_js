<script setup>
import { ref } from 'vue';
    const steep = ref(1);
    const cpt = ref(0);
    function Increment(){
        cpt.value+=steep.value;
    }
    function Reset(){
        cpt.value=0;
    }
</script>

<template>
    <div>
        <div>
            <button @click="Increment">Increment +</button>
            <button @click.right.prevent="Reset">Reset</button>
        </div>
        <div>
            <input type="number" min="1" v-model="steep" @keyup.enter="Increment">
        </div>
        <h4>{{ cpt }}</h4>
    </div>
  
</template>
<style scorped>

</style>