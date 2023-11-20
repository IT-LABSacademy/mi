<template>
  <TheNavbar />
  <Header />
  <InfoView />
  <RouterView />
  <TheEconomiya />
  <Shop />
  <TheFooter />
</template>

<script>
import { RouterView } from "vue-router";
import TheNavbar from "./components/TheNavbar.vue";
import InfoView from "./components/InfoView.vue";
import TheEconomiya from "./components/TheEconomiya.vue";
import Shop from "../src/components/home/Shop.vue";
import TheFooter from "../src/components/home/TheFooter.vue";
import Header from './components/home/Header.vue';

export default {
  components: {
    TheNavbar,
    Header,
    InfoView,
    TheEconomiya,
    Shop,
    TheFooter,
  },
};
</script>
