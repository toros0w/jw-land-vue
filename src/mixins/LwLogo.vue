<template>
  <a href="index.html" aria-label="На главную">
    <img
      :src="require(`@/assets/img/${img}`)"
      :alt="imgAlt"
      :width="imgWidth"
      :height="imgHeight"
      class="lw-logo"
    />
  </a>
</template>

<script>
export default {
  name: "LwLogo",
  props: {
    img: String,
    imgAlt: String,
    imgWidth: String,
    imgHeight: String,
  },
};
</script>

<style lang="scss" scoped>
.lw-logo {
  width: auto;
  // max-width: 65px;
  height: auto;
  max-height: 220px;
  object-fit: contain;
}
</style>
