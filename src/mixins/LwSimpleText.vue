<template>
  <span class="lw-simple-text" v-html="data.text"></span>
</template>

<script>
export default {
  name: "LwSimpleText",
  props: {
    data: Object,
  },
};
</script>

<style lang="scss" scoped>
.lw-simple-text {
  font-size: 14px;
  font-weight: 400;
  color: #333333;
}
</style>
