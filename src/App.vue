<template>
  <TheNavbar />
  <TheMabileApp />
  <TheShop />
  <RouterView />
</template>

<script>
import { RouterView } from "vue-router";
import TheNavbar from "./components/TheNavbar.vue";
import TheMabileApp from "./components/TheMabileApp.vue";
import TheShop from "./components/TheShop.vue";

export default {
  components: {
    TheNavbar,
    TheMabileApp,
    TheShop,
  },
};
</script>
