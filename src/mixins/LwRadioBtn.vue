<template>
  <div class="lw-radio-btn">
    <input type="radio" :id="data.id" :name="data.name" />
    <label :for="data.id">{{ data.title }}</label>
  </div>
</template>

<script>
export default {
  name: "LwRadioBtn",
  props: {
    data: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/extends";
:root {
  --lw-radio-btn-color: #333333;
  --lw-radio-btn-checked-color: #dedede;

  --lw-radio-btn-bg-gradient: linear-gradient(180deg, #fefefe 0%, #f6f6f6 100%);
  --lw-radio-btn-bg-color: transparent;
  --lw-radio-btn-checked-bg-color: #333333;

  --lw-radio-btn-radius: 3px;
  --lw-radio-btn-border: 1px solid #dedede;

  --lw-radio-btn-min-width: 100px;

  --lw-radio-btn-font-size: 14px;
  --lw-radio-btn-padding: 10px 20px;
}

.flex-centered-content {
  display: flex;
  align-items: center;
  justify-content: center;
}

.lw-radio-btn {
  @extend .flex-centered-content;

  input[type="radio"] {
    display: none;

    &:checked + label {
      color: var(--lw-radio-btn-checked-color);
      background: none;
      background-color: var(--lw-radio-btn-checked-bg-color);
    }
  }

  label {
    @extend .flex-centered-content;

    font-size: var(--lw-radio-btn-font-size);
    padding: var(--lw-radio-btn-padding);
    width: fit-content;
    min-width: var(--lw-radio-btn-min-width);
    color: var(--lw-radio-btn-color);
    border: var(--lw-radio-btn-border);
    border-radius: var(--lw-radio-btn-radius);
    background: var(--lw-radio-btn-bg-gradient);
    background-color: var(--lw-radio-btn-bg-color);

    cursor: pointer;
  }
}
</style>
