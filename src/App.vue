<template>
  <TheNavbar />
  <Header />
  <InfoView />
  <RouterView />
</template>

<script>
import { RouterView } from 'vue-router'
import TheNavbar from './components/TheNavbar.vue';
import Header from './components/home/Header.vue';
import InfoView from './components/InfoView.vue';

export default {
  components: {
    TheNavbar,
    Header,
    InfoView,
   
  }
}

</script>
