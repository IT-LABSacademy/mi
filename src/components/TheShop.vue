<template>
  <section class="shop-mi">
    <div class="container">
      <div class="box">
        <ul>
          <p>Комплект поставки</p>
          <p>Адаптер питания</p>
          <p>Шестигранный ключ</p>
          <p>Удлинитель для насоса</p>
          <p>Винты x 5 шт.</p>
          <p>Запасная шина</p>
          <p>Руководство пользователя</p>
          <p>Буклет с информацией</p>
        </ul>
        <h1>
          Mi Electric Scooter Pro 2
          <span>54 990 ₽</span>
        </h1>
        <img src="../components/icons/Sckuter.png" alt="" />
        <TheButton color="white">Купить</TheButton>
      </div>
    </div>
  </section>
</template>

<script>
import TheButton from "./TheButton.vue";

export default {
  components: {
    TheButton,
  },
};
</script>

<style>
@import "../assets/components/theShop.scss";
</style>
