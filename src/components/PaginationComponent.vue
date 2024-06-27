<template>
  <div class="pagination">
    <div class="lw-select lw-pagination-select">
      <select class="custom-select custom-pagination-select">
        <option value="1">1</option>
        <option value="2">2</option>
        <option value="3">3</option>
        <option value="4">4</option>
        <option value="5">5</option>
        <option value="6">6</option>
      </select>
    </div>
    <div class="pagination-wrapper">
      <button class="pagination-btn pagination-btn--hidden-xs" type="button">
        <svg width="16" height="16">
          <use xlink:href="assets/sprite.svg#icon-double-arr-l"></use>
        </svg>
      </button>
      <button class="pagination-btn pagination-btn--hidden-xs" type="button">
        <svg width="16" height="16">
          <use xlink:href="assets/sprite.svg#icon-arr-l"></use>
        </svg>
      </button>
      <button class="pagination-btn" type="button">1</button>
      <button class="pagination-btn" type="button">2</button>
      <button class="pagination-btn current" type="button">3</button>
      <button class="pagination-btn pagination-btn--hidden-xs" type="button">
        <svg width="16" height="16">
          <use xlink:href="assets/sprite.svg#icon-arr-r"></use>
        </svg>
      </button>
      <button class="pagination-btn pagination-btn--hidden-xs" type="button">
        <svg width="16" height="16">
          <use xlink:href="assets/sprite.svg#icon-double-arr-r"></use>
        </svg>
      </button>
    </div>
  </div>
</template>

<script></script>

<style lang="scss" scoped>
@import "@/styles/mixins";
@import "@/styles/extends";
.pagination {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  gap: var(--main-offset);
  margin: 30px 0;

  &-wrapper {
    display: flex;
    gap: 10px;

    @include m-b-mobile-lg-down {
      gap: 3px;
    }
  }

  &-btn {
    @extend .btn-reset;
    @extend .flex-centered-content;
    width: 36px;
    height: 36px;
    padding: 10px;
    border: 1px solid var(--lightgray);
    border-radius: 3px;
    color: var(--light);

    transition: color var(--main-transition),
      border-color var(--main-transition);

    svg {
      fill: var(--light);
      transition: fill var(--main-transition);
    }

    &:hover,
    &:focus,
    &:active,
    &.current {
      border-color: var(--success);
      color: var(--success);

      svg {
        fill: var(--success);
      }
    }
  }

  @include m-b-down(420px) {
    .lw-pagination-select {
      display: none;
    }
  }
}
</style>
