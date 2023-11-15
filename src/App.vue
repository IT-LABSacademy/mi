<template>
  <TheNavbar />
  <RouterView />
  <TheEconomiya/>
</template>

<script>
import { RouterView } from 'vue-router'
import theNavbar from './components/TheNavbar.vue';
import TheEconomiya from './components/TheEconomiya.vue';

export default {
  components: {
    theNavbar,
    RouterView,
    TheEconomiya,
}
}

</script>
