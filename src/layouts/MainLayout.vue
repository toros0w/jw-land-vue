<template>
  <MainHeader />
  <MobileMenu />
  <HeadLayout />
</template>

<script>
import HeadLayout from "./HeadLayout.vue";
import MainHeader from "./MainHeader.vue";
import MobileMenu from "./MobileMenu.vue";

export default {
  name: "MainLayout",
  components: {
    HeadLayout,
    MainHeader,
    MobileMenu,
  },
  props: {
    title: {
      type: String,
      default: "test",
    },
    desc: {
      type: String,
      default: "test",
    },
    keywords: {
      type: String,
      default: "test",
    },
  },
};
</script>

<style scoped></style>
