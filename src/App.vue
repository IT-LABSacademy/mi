<template>
  <TheNavbar />
  <RouterView />
  <TheEconomiya />
</template>

<script>
import { RouterView } from 'vue-router'
import TheNavbar from './components/TheNavbar.vue';
import TheEconomiya from './components/TheEconomiya.vue';

export default {
  components: {
    TheNavbar,
    TheEconomiya,
  }
}
</script>