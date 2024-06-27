<template>
  <div class="mobile-menu">
    <div class="mobile-menu__content">
      <div class="mobile-menu__section">
        <a href="index.html" aria-label="На главную"> <LwLogo /></a>
        <button
          class="burger mobile-menu-closer"
          type="button"
          aria-label="Закрыть меню"
        >
          <img
            src="assets/img/icon-close.svg"
            alt="Бургер"
            width="24"
            height="18"
          />
        </button>
      </div>
      <div class="mobile-menu__section">
        <small class="main-header__desc lw-text lw-text--sm lw-text--light"
          >Агентство недвижимости <br />Какое то название агентства
          недвижимости</small
        >
      </div>
      <div class="mobile-menu__section">
        <HeaderContacts />
      </div>
      <div class="mobile-menu__section">
        <UserComponent />
      </div>
      <div class="mobile-menu__section">
        <FvBtn />
      </div>
    </div>
  </div>
</template>

<script>
import LwLogo from "@/mixins/LwLogo.vue";
// import CompanySlogan from "@/components/CompanySlogan.vue";
import HeaderContacts from "@/components/HeaderContacts.vue";
import UserComponent from "@/components/UserComponent.vue";
import FvBtn from "@/components/FvBtn.vue";

export default {
  name: "MobileMenu",
  components: {
    LwLogo,
    // CompanySlogan,
    HeaderContacts,
    UserComponent,
    FvBtn,
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/mixins";
.mobile-menu {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  max-width: 100vw;
  max-width: 100dvw;
  height: 100%;
  min-height: 100vh;
  min-height: 100dvh;
  background-color: transparent;
  flex-direction: column;
  z-index: 99;
  overflow: hidden;

  display: none;

  @include m-b-tablet-down {
    &.is-open {
      display: flex;

      animation: fillBg 0.5s ease-in-out forwards;

      .mobile-menu__content {
        animation: showMenu 0.5s ease-in-out forwards;
      }
    }
  }

  @keyframes fillBg {
    0% {
      background-color: transparent;
    }

    100% {
      background-color: rgba(0, 0, 0, 0.5);
    }
  }

  @keyframes showMenu {
    0% {
      right: -100vw;
    }

    100% {
      right: 0;
    }
  }

  &__content {
    width: 100%;
    max-width: 400px;
    height: inherit;
    background-color: #ffffff;

    display: flex;
    flex-direction: column;
    padding: 0 20px;

    overflow-y: auto;

    position: absolute;
    right: -100vw;
    top: 0;
  }

  .main-header__contacts,
  .main-header__desc {
    display: flex;
    margin: 0;
  }

  &__section {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 20px 0;

    &:not(:last-child) {
      border-bottom: 1px solid #e5e5e5;
    }
  }
}
</style>
