<template>
  <TheNavbar />
  <RouterView />
  <TheFooter />
</template>

<script>
import { RouterView } from "vue-router";
import TheNavbar from "./components/TheNavbar.vue";
import TheFooter from "../src/components/home/TheFooter.vue";

export default {
  components: {
    TheNavbar,
    TheFooter,
  },
};
</script>
