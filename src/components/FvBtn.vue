<template>
  <button class="fv-btn" type="button">
    <img
      src="assets/img/icon-heart.svg"
      alt="Избранное"
      width="20"
      height="20"
    /><span>Избранное</span><span class="fv-btn-count">101</span>
  </button>
</template>

<script>
export default {
  name: "FvBtn",
};
</script>

<style lang="scss" scoped>
@import "@/styles/extends";
.fv-btn {
  @extend .btn-reset;
  @extend .flex-centered-content;
  gap: 8px;

  width: 100%;
  max-width: fit-content;
  padding: 8px 10px 6px;

  background: linear-gradient(180deg, #fefefe 0%, #f6f6f6 100%);
  border: 1px solid var(--gray);
  border-radius: 3px;

  span {
    font-size: 14px;
    font-weight: 600;
    color: var(--light);
  }

  span.fv-btn-count {
    text-decoration: underline;
    color: var(--success);
  }
}
</style>
