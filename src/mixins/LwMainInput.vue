<template>
  <div class="lw-main-input-wrapper">
    <span v-if="text" class="lw-main-input-text">{{ text }}</span>
    <input :class="modifier" type="text" :placeholder="placeholder" />
    <span v-if="note" class="lw-main-input-note">{{ note }}</span>

    <input
      v-if="secondField"
      :class="modifier"
      type="text"
      :placeholder="secondFieldPlaceholder"
    />
  </div>
</template>

<script>
export default {
  name: "LwMainInput",
  props: {
    text: String,
    modifier: String,
    placeholder: String,
    note: String,
    secondField: Boolean,
    secondFieldPlaceholder: String,
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/extends";
@import "@/styles/mixins";
:root {
  --lw-main-input-text-color: #757575;
  --lw-main-input-radius: 3px;
  --lw-main-input-color: #333333;
  --lw-main-input-bg: transparent;
  --lw-main-input-inner-offset: 4px 12px;
  --lw-main-input-border: 1px solid #dedede;
  --lw-main-input-max-width: 500px;
  --lw-main-input-min-height: 26px;
}

.lw-main-input-wrapper {
  display: flex;

  align-items: center;
  flex-grow: 1;
  gap: 10px;

  min-height: 40px;
  padding: 6px 16px;
  border-radius: 3px;
  box-shadow: 0px 4px 14px rgba(0, 0, 0, 0.04);

  @media (max-width: 534px) {
    padding: 12px;
  }

  small,
  span {
    font-size: 14px;
    font-weight: 400;
    color: var(--lw-main-input-color);
  }

  @media (max-width: 534px) {
    flex-wrap: wrap;
  }

  input {
    width: 100%;
    min-height: var(--lw-main-input-min-height);
    max-width: var(--lw-main-input-max-width);
    color: var(--lw-main-input-color);
    background-color: var(--lw-main-input-bg);
    padding: var(--lw-main-input-inner-offset);
    border-radius: var(--lw-main-input-radius);
    border: var(--lw-main-input-border);
    font-size: 14px;

    &::placeholder {
      font-size: 14px;
      color: var(--lw-main-input-color);
    }
  }
}
</style>
