<template>
  <MainHeader />
  <BreadCrumbs />
  <ObjectDetail />
</template>

<script>
import BreadCrumbs from "@/components/BreadCrumbs.vue";
import ObjectDetail from "@/sections/ObjectDetail.vue";
import MainHeader from "@/layouts/MainHeader.vue";
export default {
  name: "ObjectDetailView",
  components: {
    MainHeader,
    BreadCrumbs,
    ObjectDetail,
  },
  data() {
    return {
      title: "Детальная информация объекта",
      desc: "test",
      keywords: "test",
    };
  },
};
</script>
