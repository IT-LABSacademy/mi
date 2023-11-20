<template>
  <button class="btn" :class="color">
    <slot />
  </button>
</template>

<script>
export default {
  props: {
    color: {
      type: String,
      required: true
    },
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/base/mixins.scss';

.btn {
  font-size: 16px;
  padding: 15px 35px;
  font-family: 'G-700', sans-serif;
  border-radius: 65px;
  &.black {
    background: #222222;
    color: $brand-white;
    transition: 0.2s;

    &:hover {
      background: $white;
      color: $black;
      box-shadow: 0 0 3px $brand-white;
    }
  }

  &.white {
    background: $brand-white;
    transition: 0.2s;



    &:hover {
      background: $brand-orange;
      color: $brand-white;
      box-shadow: 0 0 3px $brand-white;
      // transform: scale(1.1);
    }
  }

  &.orange {
    background: $brand-orange;
    color: $brand-white;
    transition: 0.3s;

    &:hover {
      background: $brand-white;
      color: $brand-orange;
    }
  }
}
</style>