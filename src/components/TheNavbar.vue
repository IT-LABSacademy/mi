<template>
  <header class="header">
    <div class="container">
      <div class="left">
        <!-- logo -->
        <div class="logo">
          <img src="../assets/images/logo.svg" alt="logo">
        </div>
        

        <!-- menu -->
        <ul class="menu">
          <li v-for="item in menuArray">
            <a href="#" class="link">{{ item.name }}</a>
          </li>
        </ul>
      </div>

      <TheButton color="white">Купить</TheButton>

      <!-- burger -->
      <div class="burger" @click="isMenuOpened = !isMenuOpened">
        <i v-if="!isMenuOpened" class="fa-solid fa-bars-staggered"></i>
        <i v-else class="fa-solid fa-times"></i>
      </div>
    </div>

    <!-- mobile-menu -->
    <div class="mobile-menu" :class="{ active: isMenuOpened }">
      <ul class="menu">
        <li v-for="item in menuArray">
          <a href="#" class="link">{{ item.name }}</a>
        </li>
      </ul>

      <TheButton color="white">Купить</TheButton>
    </div>

  </header>

</template>

<script>
import TheButton from './TheButton.vue';

export default {
  components: {
    TheButton
  },
  data() {
    return {
      isMenuOpened: false,
      windowWidth: '',
      menuArray: [
        {
          name: 'o продукте'
        },
        {
          name: 'Внешний вид'
        },
        {
          name: 'Безопасность'
        },
        {
          name: 'Отзывы'
        },
        {
          name: 'FAQ'
        },
      ]
    }
  },
  methods: {
    closeMenu(e) {
      this.windowWidth = e.srcElement.innerWidth
      if (this.windowWidth > 831) {
        this.isMenuOpened = false
      }
    }
  },
  mounted() {
    window.addEventListener('resize', (e) => this.closeMenu(e))
  }
}
</script>

<style lang="scss">
@import '../assets/components/theNavbar.scss';

</style>