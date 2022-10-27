<template>
  <h3>My_vars</h3>
  <p>{{ My_vars }}</p>
  <label>someInputVars <input v-model="someInputVars" /></label>
</template>

<script setup>
let My_vars = "Hello World";
let someInputVars = "vars";
</script>

<style scoped></style>
