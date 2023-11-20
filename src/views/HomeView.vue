<template>
  <Hero />
  <TheEconomiya />
  <InfoView />
  <!-- <FAQ /> -->
  <!-- <MobileApp /> -->
</template>

<script>
import Hero from "../components/home/Hero.vue";
import FAQ from "../components/home/FAQ.vue";
import MobileApp from "../components/home/MobileApp.vue";
import TheEconomiya from '../components/home/TheEconomiya.vue'
import InfoView from "../components/home/InfoView.vue";


export default {
  components: {
    Hero,
    TheEconomiya,
    FAQ,
    MobileApp,
    InfoView
},
};
</script>
