<template>
  <MainHeader />
  <Objects />
</template>

<script>
import MainHeader from "@/layouts/MainHeader.vue";
import Objects from "@/sections/SectionObjects.vue";

export default {
  name: "IndexPageView",
  components: {
    MainHeader,
    Objects,
  },
};
</script>
