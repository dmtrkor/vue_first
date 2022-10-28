<template>
  <input v-model="password.numbers" />
  <span v-text="password.numbers" />
  <p>{{ passValidLength }}</p>

  <p>{{ validatePass }}</p>
  <p>{{ validateNum }}</p>
  <p>{{ validateAll.length }}</p>
  <p>{{ validateAll.letters }}</p>
  <p>{{ validateAll.num }}</p>
</template>

<script setup>
import { computed, reactive } from "vue";
let password = reactive({
  numbers: "",
});
let passValidLength = computed(() => {
  return password.numbers.length < 8
    ? "Пароль має містити 8 символів"
    : "Все добре";
});

let validatePass = computed(() => {
  console.log(password.numbers.match(/[A-Z]/));
  return !password.numbers.match(/[A-Z]/)
    ? "Пароль має містити A - Z"
    : "Все добре";
});
let validateNum = computed(() => {
  return !password.numbers.match(/[0-9]/)
    ? "Пароль має містити 0-9"
    : "Все добре";
});
let validateAll = computed(() => {
  return {
    length:
      password.numbers.length < 8
        ? "Пароль має містити 8 символів"
        : "Все добре",
    letters: !password.numbers.match(/[A-Z]/)
      ? "Пароль має містити A - Z"
      : "Все добре",
    num: !password.numbers.match(/[0-9]/)
      ? "Пароль має містити 0-9"
      : "Все добре",
  };
});
console.log(password.numbers);
</script>

<style scoped></style>
