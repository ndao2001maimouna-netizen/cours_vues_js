<script setup>
import { computed, reactive } from 'vue';

const cart = reactive([
    {nom:'Cahier', prix:500, quantite:22},
    {nom:'Stylo', prix:100, quantite:20},
    {nom:'Livre', prix:1500, quantite:12},
    {nom:'Taille', prix:300, quantite:13}
])

const total = computed(function(){
    return cart.reduce((somme,product)=>somme + product.prix * product.quantite,0)
})
</script>

<template>
  <section class="card">
    <h2>11 - computed()</h2>

    <ul>
      <li v-for="product in cart" :key="product.nom">
       {{product.nom}}: {{ product.prix }} × {{product.quantite}} -> {{product.prix * product.quantite}}FCFA
      </li>
    </ul>

    <h3>Total : {{total}}FCFA</h3>

    <p class="note">
      Le total se met à jour automatiquement.
    </p>
  </section>
</template>

<style scoped>
.card { padding:16px; border:1px solid #eee; border-radius:12px; }
.note { margin-top:8px; color:#555; }
</style>