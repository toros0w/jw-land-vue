<template>
  <div class="lw-note">
    <img
      src="@/assets/img/icon-note.svg"
      alt="Заметка"
      width="16"
      height="16"
    />
    <span>{{ text }}</span>
  </div>
</template>

<script>
export default {
  name: "LwNote",
  props: {
    text: String,
  },
};
</script>

<style lang="scss" scoped>
.lw-note {
  display: flex;
  align-items: center;
  max-width: 550px;
  img {
    width: 16px;
    min-width: 16px;
    height: 16px;
    min-height: 16px;
    margin-right: 8px;
  }

  span {
    font-size: 14px;
    font-weight: 400;
    color: #757575;
  }
}
</style>
