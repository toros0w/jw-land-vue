<template>
  <div :class="modifier ? modifier : 'lw-control-group'">
    <template v-for="ctrl in ctrls" :key="ctrl.type">
      <span v-if="ctrl.type === 'group-title'" class="lw-control-group-title">{{
        ctrl.text
      }}</span>
      <component :is="getComponent(ctrl.type)" :data="ctrl" v-else></component>
    </template>
  </div>
</template>

<script>
import LwRadioBtn from "./LwRadioBtn.vue";
import LwBtn from "@/mixins/LwBtn.vue";
import LwSwitcher from "@/mixins/LwSwitcher.vue";
import LwMainInput from "@/mixins/LwMainInput.vue";
import LwTextarea from "@/mixins/LwTextarea.vue";
import LwLogo from "@/mixins/LwLogo.vue";
import LwSelect from "@/mixins/LwSelect.vue";
import LwMultiple from "@/mixins/LwMultiple.vue";
import LwSimpleText from "@/mixins/LwSimpleText.vue";
import LwMedia from "@/mixins/LwMedia.vue";
import LwNote from "@/mixins/LwNote.vue";
import LwMultipleChecker from "@/mixins/LwMultipleChecker.vue";
import LwCheckbox from "@/mixins/LwCheckbox.vue";
import LwCheckboxGroup from "@/mixins/LwCheckboxGroup.vue";

export default {
  name: "LwControlGroup",
  components: {
    LwRadioBtn,
    LwBtn,
    LwSwitcher,
    LwMainInput,
    LwTextarea,
    LwLogo,
    LwSelect,
    LwMultiple,
    LwSimpleText,
    LwMedia,
    LwNote,
    LwMultipleChecker,
    LwCheckbox,
    LwCheckboxGroup,
  },
  props: {
    ctrls: {
      type: Array,
      required: true,
    },
    modifier: {
      type: String,
      default: null,
    },
  },
  methods: {
    getComponent(type) {
      const components = {
        radio: "LwRadioBtn",
        button: "LwBtn",
        switcher: "LwSwitcher",
        text: "LwMainInput",
        textarea: "LwTextarea",
        logo: "LwLogo",
        select: "LwSelect",
        multiple: "LwMultiple",
        "simple-text": "LwSimpleText",
        media: "LwMedia",
        note: "LwNote",
        "multiple-checker": "LwMultipleChecker",
        checkbox: "LwCheckbox",
        "checkbox-group": "LwCheckboxGroup",
      };
      return components[type] || null;
    },
  },
};
</script>

<style lang="scss" scoped>
.lw-control-group {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
  gap: 10px 20px;
}
</style>
