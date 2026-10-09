<script setup>
import {reactive, ref } from 'vue';

const products = ref([
    {id:1, nom:'Cahier', prix:500, quantite:22},
    {id:2,nom:'Stylo', prix:100, quantite:20},
    {id:3,nom:'Livre', prix:1500, quantite:12},
    {id:4,nom:'Taille', prix:300, quantite:13}

]);
const supprime = (id)=>{
    products.value=products.value.filter((p)=>p.id != id)
}



</script>

<template>
  <section class="card">
    <h2>13 - Lists</h2>

    <ul>
      <li v-for="p in products" :key="p.id">
       {{p.nom }} - {{ p.prix}} FCFA
        <button @click="supprime(p.id)">❌</button>
      </li>
    </ul>
  </section>
</template>

<style scoped>
.card { padding:16px; border:1px solid #eee; border-radius:12px; }
li { display:flex; justify-content:space-between; width:250px; }
button { border:none; background:none; cursor:pointer; }
</style>