<template>
<<<<<<< HEAD
     <RouterView />
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

=======
  <TheNavbar />
  <RouterView />
</template>

<script>
import { RouterView } from 'vue-router'
import TheNavbar from './components/TheNavbar.vue';

export default {
  components: {
    TheNavbar
  }
}
</script>
>>>>>>> 92007e25f128fdda53fcf2f7cf5afeb42193c28d
