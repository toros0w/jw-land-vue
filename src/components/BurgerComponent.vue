<template>
  <button
    class="burger mobile-menu-opener"
    type="button"
    aria-label="Открыть меню"
  >
    <img src="assets/img/icon-burger.svg" alt="Бупгер" width="24" height="18" />
  </button>
</template>

<script>
export default {
  name: "BurgerComponent",
};
</script>

<style lang="scss" scoped>
@import "@/styles/extends";
.burger {
  @extend .btn-reset;
  @extend .flex-centered-content;

  cursor: pointer;
}
</style>
