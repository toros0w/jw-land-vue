<template>
  <div class="img-frame">
    <img :src="`/assets/img/${img}`" alt="Избранное" width="80" height="80" />
  </div>
</template>

<script>
export default {
  name: "ImgFrame",
  props: {
    img: {
      type: String,
      required: true,
    },
  },
};
</script>

<style lang="scss" scoped>
.img-frame {
  position: relative;
  border: 1px solid #dedede;
  border-radius: 3px;

  &::after {
    position: absolute;
    bottom: -1px;
    left: -1px;
    width: 26px;
    height: 12px;

    content: "";

    border-radius: 0 5px 0 3px;
    border: 1px solid var(--object-preview-card-main-color);
    background-color: #ffffff;

    background-image: url("@/assets/img/icon-logo.svg");
    background-size: 12px auto;
    background-repeat: no-repeat;
    background-position: center;
    z-index: 2;
  }

  img {
    width: 80px;
    height: 80px;
    object-fit: contain;
    object-position: center;
  }
}
</style>
