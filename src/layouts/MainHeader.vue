<template>
  <header class="main-header">
    <div class="lw-container main-header__container">
      <LwLogo
        img="icon-logo.svg"
        imgAlt="JoyWork"
        imgHeight="40"
        imgWidth="125"
      />
      <CompanySlogan />
      <HeaderContacts />
      <FvBtn />
      <UserComponent />
      <BurgerComponent />
    </div>
  </header>
</template>

<script>
import CompanySlogan from "@/components/CompanySlogan.vue";
import HeaderContacts from "@/components/HeaderContacts.vue";
import LwLogo from "@/mixins/LwLogo.vue";
import FvBtn from "@/components/FvBtn.vue";
import UserComponent from "@/components/UserComponent.vue";
import BurgerComponent from "@/components/BurgerComponent.vue";

export default {
  name: "MainHeader",
  components: {
    LwLogo,
    CompanySlogan,
    HeaderContacts,
    FvBtn,
    UserComponent,
    BurgerComponent,
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/extends";
@import "@/styles/mixins";
.main-header {
  padding: 20px 0;

  &__container {
    display: flex;
    align-items: center;
    gap: 20px;
  }

  .lw-logo {
    margin-right: 10px;
  }

  &__desc {
    max-width: 200px;

    @include m-b-tablet-lg-down {
      max-width: fit-content;
    }

    @include m-b-mobile-lg-down {
      display: none;
    }
  }

  &__contacts {
    @extend .flex-column;
    gap: 5px;
    margin: 0 auto;

    @include m-b-tablet-lg-down {
      display: none;
    }
  }

  .fv-btn {
    margin: 0 auto;

    @include m-b-down(1140px) {
      display: none;
    }
  }

  .user {
    max-width: 270px;
    margin-left: auto;

    @include m-b-tablet-down {
      display: none;
    }
  }

  .burger {
    display: none;
    margin-left: auto;
    z-index: 10;

    /* @include m-b-tablet-down {
      display: flex;
    } */
  }
}
</style>
