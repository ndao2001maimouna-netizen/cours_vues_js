<script setup>
    const momtant = 100000
    const ans = new Date() .getFullYear();
    const person = {fullName:"Maimouna Ndao", role: "Etudiante"}
    const prime = 0.5;
</script>
<template>
     <section class="card">
     <h1>02_Interpolation</h1>
     <p>Deuxieme composant Vue (SFC)</p>
    <div>
        <li>
        <ul>Nom: {{ person.fullName  }} </ul>
        <ul>Role: {{ person.role  }} </ul>
        <ul>Montant: {{ momtant }}</ul>
        <ul>Annee: {{ ans }}</ul>
        <ul>Salaire Net: {{ momtant + momtant*prime }}</ul>
        </li>
    </div>
  </section>
</template>

<style scoped>
    .card{
        background: #e0bfbf;
    }
</style>