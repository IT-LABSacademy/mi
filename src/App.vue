<template>
  <TheNavbar />
  <InfoView />
  <RouterView />
</template>

<script>
import { RouterView } from 'vue-router'
import TheNavbar from './components/TheNavbar.vue';
import InfoView from './components/InfoView.vue';

export default {
  components: {
    TheNavbar,
    InfoView
}
}
</script>
