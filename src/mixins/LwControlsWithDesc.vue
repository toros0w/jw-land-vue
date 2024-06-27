<template>
  <div :class="data.modifier ? data.modifier : 'lw-controls-with-desc'">
    <span>{{ data.text }}</span>
    <div class="lw-controls-wrapper">
      <div v-for="group in data.groups" :key="group[0].type">
        <LwControlGroup :ctrls="group" />
      </div>
    </div>
  </div>
</template>

<script>
import LwControlGroup from "./LwControlGroup.vue";

export default {
  name: "LwControlsWithDesc",
  components: {
    LwControlGroup,
  },
  props: {
    data: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped>
/* .lw-controls-with-desc {
}

.lw-controls-wrapper {
} */
</style>
