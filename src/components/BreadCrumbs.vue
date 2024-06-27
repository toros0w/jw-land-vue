<template>
  <div class="lw-container">
    <div class="breadcrumbs">
      <a class="lw-text lw-text--medi lw-text--light" href="index.html"
        >Жилые комплексы</a
      ><a class="lw-text lw-text--medi lw-text--light" href="index.html"
        >Жилые комплексы Санкт-Петербурга</a
      >
      <a class="lw-text lw-text--medi lw-text--light" href="index.html"
        >Жилые комплексы</a
      ><a class="lw-text lw-text--medi lw-text--light" href="index.html"
        >Жилые комплексы</a
      >
      <span class="lw-text lw-text--medi lw-text--success">ЖК «Брустника»</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "BreadCrumbs",
};
</script>

<style lang="scss" scoped>
@import "@/styles/extends";
.breadcrumbs {
  @extend .flex-wrap;
  gap: 5px;
  padding: var(--main-offset) 0;

  a {
    position: relative;
    display: flex;
    width: fit-content;
    padding-right: 35px;

    &::after {
      position: absolute;
      top: 50%;
      right: 5px;
      transform: translateY(-50%);
      content: "";
      width: 20px;
      height: 18px;

      background-image: url("@/assets/img/icon-breadcrumb-arr.svg");
      background-repeat: no-repeat;
      background-size: contain;
      background-position: center;
    }
  }
}
</style>
