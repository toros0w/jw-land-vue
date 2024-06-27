<template>
  <div class="lw-multiple-row">
    <lw-control-group :ctrls="controls" />
  </div>
</template>

<script>
import LwControlGroup from "./LwControlGroup.vue";

export default {
  name: "LwMultiple",
  components: {
    LwControlGroup,
  },
  props: {
    controls: Array,
  },
};
</script>

<style scoped></style>
