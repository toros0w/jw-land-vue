<template>
  <component :is="tag" :href="href" :class="cls">
    <template v-if="icon && iconSide !== 'right'">
      <img
        :src="require(`@/assets/img/${icon}`)"
        :alt="iconAlt"
        :width="iconWidth"
        :height="iconHeight"
      />
    </template>
    <span v-if="text">{{ text }}</span>
    <template v-if="icon && iconSide === 'right'">
      <img
        :src="require(`@/assets/img/${icon}`)"
        :alt="iconAlt"
        :width="iconWidth"
        :height="iconHeight"
      />
    </template>
  </component>
</template>

<script>
export default {
  name: "LwBtn",
  props: {
    tag: {
      type: String,
      required: true,
    },
    href: {
      type: String,
      required: true,
    },
    cls: String,
    text: String,
    icon: String,
    iconSide: String,
    iconAlt: String,
    iconWidth: String,
    iconHeight: String,
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/ui-components/lw-simple-btn";
:root {
  --lw-main-btn-font-size: 14px;
  --lw-main-btn-font-weight: 400;

  --lw-main-btn-padding: 8px 12px;
  --lw-main-btn-primary-color: #ffffff;
  --lw-main-btn-secondary-color: #4caf50;
  --lw-main-btn-radius: 3px;

  --lw-main-btn-transition: var(--main-transition);
}

.lw-main-btn {
  display: flex;
  align-items: center;
  justify-content: center;

  min-height: 40px;

  font-size: var(--lw-main-btn-font-size);
  font-weight: var(--lw-main-btn-font-weight);

  border: 1px solid transparent;
  padding: var(--lw-main-btn-padding);
  color: var(--lw-main-btn-primary-color);
  background-color: var(--lw-main-btn-secondary-color);
  border-radius: var(--lw-main-btn-radius);

  transition: background-color var(--lw-main-btn-transition),
    border var(--lw-main-btn-transition), color var(--lw-main-btn-transition);

  &:hover,
  &:focus {
    border-color: 1px dashed var(--lw-main-btn-secondary-color);
    background-color: transparent;
    color: var(--lw-main-btn-secondary-color);
  }

  cursor: pointer;

  &--media {
    width: 100%;
    height: 100%;
    background: linear-gradient(180deg, #fefefe 0%, #f6f6f6 100%);
    border: 1px dashed #dedede;
    border-radius: 3px;

    img {
      max-width: 50px;
    }
  }

  &--outlined {
    border-color: 1px dashed var(--lw-main-btn-secondary-color);
    background-color: transparent;
    color: var(--lw-main-btn-secondary-color);

    &:hover,
    &:focus {
      color: var(--lw-main-btn-primary-color);
      background-color: var(--lw-main-btn-secondary-color);
    }
  }
}
</style>
