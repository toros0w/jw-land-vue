<template>
  <div>
    <div v-if="currentPage === 'index'">
      <section>
        <h1>{{ title }}</h1>
        <IndexPageView />
      </section>
    </div>
    <div v-if="currentPage === 'object-detail-map'">
      <section>
        <ObjectDetailMapView />
      </section>
    </div>
    <div v-if="currentPage === 'object-detail'">
      <ObjectDetailView />
    </div>
  </div>
</template>

<script>
import IndexPageView from "@/views/IndexPageView.vue";
import ObjectDetailMapView from "@/views/ObjectDetailMapView.vue";
import ObjectDetailView from "@/views/ObjectDetailView.vue";

export default {
  name: "App",
  components: {
    IndexPageView,
    ObjectDetailMapView,
    ObjectDetailView,
  },
  data() {
    return {
      currentPage: "object-detail",
      title: "",
      desc: "",
      keywords: "",
    };
  },
  created() {
    this.updateMeta();
  },
  watch: {
    currentPage() {
      this.updateMeta();
    },
  },
  methods: {
    updateMeta() {
      switch (this.currentPage) {
        case "index":
          this.title = "Главная";
          this.desc = "";
          this.keywords = "";
          break;
        case "object-detail-map":
          this.title = "Детальная карта объекта";
          this.desc = "";
          this.keywords = "";
          break;
        case "object-detail":
          this.title = "Детальная информация объекта";
          this.desc = "";
          this.keywords = "";
          break;
      }
      document.title = this.title;
    },
  },
};
</script>

<style lang="scss">
@import "@/styles/main.scss";
@import "styles/extends";
@import "styles/mixins";
@import "styles/ui-components/lw-main-slider.scss";
@import "styles/ui-components/lw-textarea.scss";
</style>
