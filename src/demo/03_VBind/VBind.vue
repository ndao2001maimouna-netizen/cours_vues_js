<script setup>
const image = "https://i.pinimg.com/736x/41/25/4c/41254c1090b340cd4df0e415b72915e5.jpg"
const btn = false

</script>

<template>
    <section class="card">
     <h1>03_VBind</h1>
     <p>troisieme composant Vue (SFC)</p>
       <div>
         <img :src="image" alt="">
         <button :disabled="1 < 2">Clic Me</button>
       </div>
    </section>
  
</template>

<style scoped>

</style>