<template>
  <div class="lw-textarea">
    <label
      v-if="data.label"
      :for="data.id"
      class="lw-textarea-title"
      v-html="data.label"
    ></label>
    <textarea :id="data.id"></textarea>
  </div>
</template>

<script>
export default {
  name: "LwTextarea",
  props: {
    data: Object,
  },
};
</script>

<style lang="scss" scoped>
:root {
  --lw-textarea-height: 100px;
  --lw-textarea-max-width: 500px;
  --lw-textarea-radius: 6px;
  --lw-textarea-border: 1px solid #dedede;
  --lw-textarea-inner-offset: 8px 12px;
  --lw-textarea-color: #333333;
}

.lw-textarea {
  display: flex;
  flex-direction: column;
  width: 100%;
  max-width: var(--lw-textarea-max-width);

  &-title {
    display: inline-block;
    margin-bottom: 10px;
    font-size: 14px;
    color: #757575;
  }

  textarea {
    resize: none;
    width: 100%;
    height: var(--lw-textarea-height);

    border-radius: var(--lw-textarea-radius);
    border: var(--lw-textarea-border);

    padding: var(--lw-textarea-inner-offset);
    color: var(--lw-textarea-color);
  }
}
</style>
