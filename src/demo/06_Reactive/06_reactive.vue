<script setup>
import { reactive, ref } from 'vue';
const ajoutermontant = ref();
const cpt = ref(0);

 const moi = reactive({nom:"Maimouna", tel:"764851797", solde:1000});
 function ajouter( montant){
    if(cpt.value < 10){
      moi.solde+= montant
      cpt.value++
    }
   ajoutermontant.value=0
    return   
 }

</script>

<template>
  <section class="card">
    <h2>09 - reactive()</h2>

    <div class="box">
      <p><strong>Nom :</strong>{{moi.nom}}</p>
      <p><strong>Téléphone :</strong> {{moi.tel}} </p>
      <p><strong>Solde :</strong> {{moi.solde}}FCFA</p>
    </div>

    <div class="actions">
      <button @click="ajouter(5000)">+5 000</button>
      <button @click="ajouter(10000)">+10 000</button>
      <input type="number" placeholder="Autres" v-model="ajoutermontant" @keyup.enter="ajouter(ajoutermontant)">
    </div>
    <p>{{ cpt }}</p>
    <p class="note">
      <code>reactive()</code> est idéal pour les objets complexes.
    </p>
  </section>
</template>

<style scoped>
.card { padding:16px; border:1px solid #eee; border-radius:12px; }
.box { padding:12px; background:#fafafa; border-radius:10px; }
.actions { display:flex; gap:10px; margin-top:10px; }
button { padding:8px 10px; border:1px solid #ddd; border-radius:8px; }
.note { margin-top:8px; color:#555; }
</style>