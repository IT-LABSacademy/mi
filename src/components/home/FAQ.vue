<template>
  <section class="acardion">
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
        <div class="accordion">
          <!-- item -->
          <div class="adn" v-for="(item, index) in accordionArray" :key="item">
            <div class="title" @click="openAcc(index)">
              <h2 class="accordion__label">
                {{ item.question }}
              </h2>
              <p><i class="fa-solid fa-chevron-down"></i></p>
            </div>
            <div class="border"></div>
            <div class="accordion__content" v-if="item.isOpen">
              <p>
                {{ item.answer }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>

  </section>
</template>

<script>
import TheButton from '../TheButton.vue';

export default {
  components: {
    TheButton,
  },
  data() {
    return {
      accordionArray: [
        {
          question: 'На него нужны права категории M?',
          answer: `Продуманный угол рассеивания света позволяет сохранять хорошую видимость, не ослепляя других участников движения.`,
          isOpen: false,
        },
        {
          question: 'У меня вес 135 кг, выдержит ли этот самокат?',
          answer: `Самокат определенно выдержит и будет ехать, но не с максимальной скоростью.`,
          isOpen: false,
        },
        {
          question: 'Есть ли влагозащита?',
          answer: ` Электросамокат имеет степень защиты IP54. Он защищен от попадания пыли и брызг, падающих в любом
          направлении. Погружение в воду может привести к поломке.`,
          isOpen: false,
        },
        {
          question: 'Это версия для Китая или Европы?',
          answer: `Это Европейская версия, со всеми обновлениями и евро-вилкой.`,
          isOpen: false,
        },
      ]
    }
  },
  methods: {
    openAcc(index) {
      this.accordionArray[index].isOpen = !this.accordionArray[index].isOpen
    }
  }
}
</script>

<style lang="scss" scoped>
@import './styles/faq.scss';
</style>