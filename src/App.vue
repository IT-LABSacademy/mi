<template>
  <TheNavbar />
  <InfoView />
  <RouterView />
  <TheEconomiya />
</template>

<script>
import { RouterView } from 'vue-router'
import TheNavbar from './components/TheNavbar.vue';
import InfoView from './components/InfoView.vue';
import TheEconomiya from './components/TheEconomiya.vue';

export default {
  components: {
    TheNavbar,
    InfoView,
    TheEconomiya,
  }
}

</script>
