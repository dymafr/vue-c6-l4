<template>
  <ul>
    <li v-for="(fruit, index) in fruits">{{ `${index} - ${fruit}` }}</li>
  </ul>

  <ul>
    <li v-for="({ prenom, notes }, index) of utilisateurs">
      {{ `${index} : ${prenom}` }}
      <span v-for="note in notes">{{ note }} / </span>
    </li>
  </ul>
  <ul>
    <li v-for="(valeur, cle, index) of voiture">
      {{ `${index} : ${valeur} - ${cle}` }}
    </li>
  </ul>
  <ul>
    <li v-for="n in 4">Bonjour !</li>
  </ul>
</template>

<script setup lang="ts">
import { reactive } from 'vue';

const fruits = reactive(['fraise', 'pomme', 'kiwi']);
const utilisateurs = reactive([
  { prenom: 'Jean', notes: [14, 15, 18] },
  { prenom: 'Paul', notes: [12, 10, 8] },
  { prenom: 'Pierre', notes: [3, 15, 18] },
]);
const voiture = {
  roues: 4,
  prix: 4000,
};
</script>

<style scoped lang="scss"></style>
