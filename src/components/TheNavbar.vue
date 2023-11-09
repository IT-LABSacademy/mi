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

  <header class="acardion">
        <div class="container">
            <!-- Часто задаваемые вопросы -->
            <div class="wrapper">

              <div class="left">
                <div class="faq">
                  <h1>Часто задаваемые вопросы</h1>
              </div>
              <div class="scooterMI">
                <div class="text">
                  <p>Все ваши часто задаваемые вопросы o электросамокате Mi Scooter Pro 2.</p>
                  <p>Если у вас есть собственный вопрос - задайте его через форму обратной связи.</p>
                </div>
              </div>
              <div class="btn">
                <TheButton color="white" class="question">Задать вопрос</TheButton>
              </div>
            </div>

            <!-- right accordion -->
            <div class="right">
              <div class="accordion">
                <div class="adn">
                  <input type="radio" name="example_accordion" id="section-1" class="accordion__input">
                  <label for="section-1" class="accordion__label">На него нужны права категории M?</label>
                  <div class="border"></div>
                  <div class="accordion__content">
                    <p>
                      Продуманный угол рассеивания света позволяет сохранять хорошую видимость, не ослепляя других участников движения.
                    </p>
                  </div>
                </div>
                <div class="adn">
                  <input type="radio" name="example_accordion" id="section-2" class="accordion__input">
                  <label for="section-2" class="accordion__label">У меня вес 135 кг, выдержит ли этот самокат?</label>
                  <div class="border"></div>
                  <div class="accordion__content">
                    <p>
                      Самокат определенно выдержит и будет ехать, но не с максимальной скоростью.
                    </p>
                  </div>
                </div>
                <div class="adn">
                  <input type="radio" name="example_accordion" id="section-3" class="accordion__input">
                  <label for="section-3" class="accordion__label">Есть ли влагозащита?</label>
                  <div class="border"></div>
                  <div class="accordion__content">
                    <p>
                      Электросамокат имеет степень защиты IP54. Он защищен от попадания пыли и брызг, падающих в любом направлении. Погружение в воду может привести к поломке. 
                    </p>
                  </div>
                </div>
                <div class="adn">
                  <input type="radio" name="example_accordion" id="section-4" class="accordion__input">
                  <label for="section-4" class="accordion__label">Это версия для Китая или Европы?</label>
                  <div class="border"></div>
                  <div class="accordion__content">
                    <p>
                      Это Европейская версия, со всеми обновлениями и евро-вилкой.
                    </p>
                  </div>
                </div>

              </div>
            </div>
          </div>
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
          name: 'О продукте'
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