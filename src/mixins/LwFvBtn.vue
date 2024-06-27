<template>
  <button
    :class="['lw-fv-btn', { active: active, 'lw-fv-btn--simple': !text }]"
    @click="onClick"
    type="button"
    aria-label="Избранное"
  >
    <span v-if="text" class="lw-text lw-text--light">В избранное</span>
  </button>
</template>

<script>
export default {
  name: "LwFvBtn",
  props: {
    state: String,
    text: String,
  },
  data() {
    return {
      active: false,
    };
  },
  methods: {
    onClick() {
      this.active = !this.active;
    },
  },
  mounted() {
    this.active = this.state;
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/extends";
@import "@/styles/mixins";
.lw-fv-btn {
  @extend .btn-reset;
  @extend .flex-centered-content;

  width: fit-content;
  min-width: 40px;
  height: 40px;
  min-width: 40px;
  background-image: url("@/assets/img/icon-heart-gray.svg");
  background-repeat: no-repeat;
  background-size: 24px;
  background-position: left;

  &--simple {
    background-position: center;
  }

  span {
    white-space: nowrap;
    padding-left: 32px;
  }

  &.active {
    background-image: url("@/assets/img/icon-heart-red-filled.svg");
  }
}
</style>
