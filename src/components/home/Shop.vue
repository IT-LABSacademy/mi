<template>
  <section class="shop">
    <div class="container">
      <div class="buy-box">
        <!-- Left -->
        <div class="left">
          <!-- Text -->
          <h1>
            Mi Electric Scooter Pro 2
            <span>54 990 ₽</span>
          </h1>

          <!-- Button -->
          <TheButton color="white">Купить</TheButton>
        </div>

        <!-- Right -->
        <div class="right">
          <ul>
            <h2>Комплект поставки</h2>
            <li>Адаптер питания</li>
            <li>Буклет с информацией</li>
            <li>Шестигранный ключ</li>
            <li>Удлинитель для насоса</li>
            <li>Винты x 5 шт.</li>
            <li>Запасная шина</li>
            <li>Руководство пользователя</li>
            <li>Буклет с информацие</li>
          </ul>

          <img src="../../assets/images/Scooter.png" alt="" />
        </div>
      </div>
    </div>
  </section>
</template>

<!-- Script -->
<script>
import TheButton from "../TheButton.vue";

export default {
  components: {
    TheButton,
  },
};
</script>

<!-- Style -->
<style>
@import "./styles/shop.scss";
</style>
