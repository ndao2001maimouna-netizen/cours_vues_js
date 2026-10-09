<script setup>
import { ref } from 'vue';

const fullName = ref('');
const phoneNumber = ref('');
const tabs = ref([]);
function addContact(){
    if(!fullName.value.trim() || !phoneNumber.value.trim())
        return
    tabs.value.unshift({
        id: crypto.randomUUID(),
        fullName:fullName.value,
        phoneNumber:phoneNumber.value
    })
    fullName.value="";
    phoneNumber.value="";
}

</script>

<template>
  <div class="card">
    <h3>EventForm</h3>

    <form class="form" @submit.prevent="addContact">
      <input class="input" placeholder="Nom complet" v-model="fullName"/>
      <input class="input" placeholder="Téléphone" v-model="phoneNumber" />
      <button type="submit">Enregistrer</button>
    </form>
        {{ tabs }}
    <p class="note">
        <!-- @ C'est event submit ca nous permet de recuperer. En gros ca nous permet de recuperer et soumettre-->
        <!-- v-model permet de créer une liaison bidirectionnelle pour synchroniser 
        automatiquement la valeur d'un champ HTML avec une variable déclarée dans le JavaScript      -->
 Démo : <code>v-model</code>, <code>@submit</code>.
    </p>
  </div>
</template>

<style scoped>
.card { padding: 14px; border: 1px solid #eee; border-radius: 12px; margin-top: 12px; }
.form { display: flex; gap: 10px; flex-wrap: wrap; }
.input { padding: 8px 10px; border: 1px solid #ddd; border-radius: 10px; min-width: 220px; }
button { padding: 8px 10px; border-radius: 10px; border: 1px solid #ddd; background: white; }
.empty { margin-top: 10px; color: #666; }
.list { margin: 10px 0 0; padding-left: 18px; }
.note { margin-top: 8px; color: #555; }
</style>