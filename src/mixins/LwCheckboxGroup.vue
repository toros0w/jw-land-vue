<template>
  <div class="lw-checkbox-group">
    <div class="lw-checkbox-group__header">
      <LwCheckbox
        :data="{
          type: 'checkbox',
          label: data.mainCheckboxLabel,
          id: data.mainCheckboxId,
          cls: 'lw-checkbox-group-head-control',
        }"
      />
    </div>
    <LwControlGroup :ctrls="data.checkboxes" />
  </div>
</template>

<script>
import LwCheckbox from "./LwCheckbox.vue";
import LwControlGroup from "./LwControlGroup.vue";

export default {
  name: "LwCheckboxGroup",
  components: {
    LwCheckbox,
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

<style lang="scss" scoped>
.lw-checkbox-group {
  width: 100%;
  max-width: 1000px;

  &__header {
    margin-bottom: 15px;
  }
}
</style>
