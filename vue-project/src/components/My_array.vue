<template>
  <h1>People</h1>
  <ul>
    <li v-for="(people, index) in peoples" :key="index">
      {{ people }} <button v-on:click="peoples.splice(index, 1)">-</button>
    </li>
  </ul>
  <input id="newName" />
  <button @click="addPeople">+</button>
</template>
<script setup>
console.log("index");

import { ref } from "vue";
let peoples = ref([]);
console.log(peoples);
const addPeople = function () {
  peoples.value.push(document.getElementById("newName").value);

  console.log(peoples);
};
</script>
<style>
ul {
  list-style-type: none;
}
</style>
