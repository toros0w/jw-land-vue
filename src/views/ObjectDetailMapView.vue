<template>
  <div>
    <MainHeader />
    <BreadCrumbs />
    <ObjectDetailMap />
  </div>
</template>

<script>
import ObjectDetailMap from "@/sections/ObjectDetailMap.vue";
import BreadCrumbs from "@/components/BreadCrumbs.vue";
import MainHeader from "@/layouts/MainHeader.vue";

export default {
  name: "ObjectDetailMapView",
  components: {
    MainHeader,
    BreadCrumbs,
    ObjectDetailMap,
  },
};
</script>
