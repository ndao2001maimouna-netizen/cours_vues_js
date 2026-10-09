
<script setup>
const message = "ande dem wala ande soukh"

</script>


<template>
 <section class="card">
     <h1>01_Hello_World</h1>
     <p>Premier composant Vue (SFC)</p>
     <div class="box">
     <strong>Message: </strong>{{ message .toUpperCase()}}
  </div>
</section>
</template>

<style scoped>
  .card{
    padding: 16px;
    border: 1px solid #eee;
    border-radius: 12px;
  }
  .box{
    margin: 10px;
    padding: 12px;
    border: 1px dashed #ccc;
    border-radius: 10px;
  }
</style>