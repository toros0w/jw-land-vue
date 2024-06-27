<template>
  <div class="lw-main-slider">
    <div class="swiper">
      <div class="swiper-wrapper">
        <div class="swiper-slide" v-for="slide in slides" :key="slide.id">
          <img
            :src="require(`@/assets/img/${slide.img}`)"
            :alt="slide.alt"
            width="550"
            height="550"
          />
        </div>
      </div>

      <div class="swiper-button-prev"></div>
      <div class="swiper-button-next"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "LwMainSlider",
  props: {
    slides: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/extends";
.lw-main-slider {
  height: fit-content;
  max-height: 550px;

  .swiper-button-next:after {
    padding-left: 4px;
  }

  .swiper-button-prev::after {
    padding-right: 4px;
  }

  .swiper-button-next,
  .swiper-button-prev {
    color: var(--dark);

    &::after {
      font-size: 20px;
      width: 32px;
      min-width: 32px;
      height: 32px;
      background-color: #ffffff;
      border-radius: 50%;
      display: flex;

      align-items: center;
      justify-content: center;

      box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;
    }
  }

  .swiper-slide {
    width: 100%;
    box-sizing: border-box;

    @extend .img-frame-lg;

    img {
      display: flex;
      width: 100%;
      height: auto;
      max-height: 550px;
      object-fit: cover;
      aspect-ratio: 1 / 1;
    }
  }
}
</style>
