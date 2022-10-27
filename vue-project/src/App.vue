<script>
//import My_first from "./components/My_first.vue";
//import My_second from "./components/My_second.vue";
import My_array from "./components/My_array.vue";
import My_vars from "./components/Vars/My_vars.vue";

export default {
  components: { My_array, My_vars },
};
</script>
<template>
  <header>
    <img
      alt="Vue logo"
      class="logo"
      src="./assets/logo.svg"
      width="125"
      height="125"
    />

    <div class="wrapper"></div>
    <div><My_vars></My_vars></div>
  </header>

  <main><My_array></My_array></main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
