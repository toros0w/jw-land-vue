<template>
  <div :class="['lw-switcher', data.modifier]">
    <input
      :type="data.switcherType === 'radio' ? 'radio' : 'checkbox'"
      :id="data.id"
      :name="data.name"
    />
    <label :for="data.id">
      <span v-html="data.title"></span>
    </label>
  </div>
</template>

<script>
export default {
  name: "LwSwitcher",
  props: {
    data: Object,
  },
};
</script>

<style lang="scss" scoped>
:root {
  --lw-switcher-text-color: #333333;
  --lw-switcher-text-font-size: 14px;

  --lw-switcher-box-shadow: inset 0px 2px 2px rgba(0, 0, 0, 0.15);
  --lw-switcher-bg-color: #dddddd;
  --lw-switcher-checked-bg-color: #4caf50;

  --lw-switcher-width: 40px;
  --lw-switcher-height: 26px;
  --lw-switcher-radius: 15px;
  --lw-switcher-offset-width: 14px;
  --lw-switcher-offset: calc(
    var(--lw-switcher-width) + var(--lw-switcher-offset-width)
  );

  --lw-switcher-pin-bg-color: #ffffff;
  --lw-switcher-pin-width: 20px;
  --lw-switcher-pin-height: 20px;
  --lw-switcher-pin-box-shadow: 0px 1px 3px rgba(0, 0, 0, 0.15);
  --lw-switcher-pin-radius: 50%;

  --lw-switcher-pin-posX: 3px;
  --lw-switcher-checked-pin-posX: calc(
    var(--lw-switcher-width) - var(--lw-switcher-pin-posX) -
      var(--lw-switcher-pin-width)
  );

  --lw-switcher-transition: 0.2s ease-in;
}

.lw-switcher {
  input {
    display: none;

    &:checked + label {
      &::before {
        background-color: var(--lw-switcher-checked-bg-color);
      }

      &::after {
        left: var(--lw-switcher-checked-pin-posX);
      }
    }
  }

  label {
    position: relative;
    display: flex;
    align-items: center;
    width: fit-content;

    font-size: var(--lw-switcher-text-font-size);
    color: var(--lw-switcher-text-color);
    padding-left: var(--lw-switcher-offset);

    min-height: var(--lw-switcher-height);

    cursor: pointer;

    &::before,
    &::after {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);

      content: "";
    }

    &::before {
      left: 0;
      width: var(--lw-switcher-width);
      height: var(--lw-switcher-height);

      background-color: var(--lw-switcher-bg-color);
      box-shadow: var(--lw-switcher-box-shadow);
      border-radius: var(--lw-switcher-radius);

      transition: background-color var(--lw-switcher-transition);
    }

    &::after {
      left: var(--lw-switcher-pin-posX);
      width: var(--lw-switcher-pin-width);
      height: var(--lw-switcher-pin-height);

      background-color: var(--lw-switcher-pin-bg-color);
      box-shadow: var(--lw-switcher-pin-box-shadow);
      border-radius: var(--lw-switcher-pin-radius);

      transition: left var(--lw-switcher-transition);
    }
  }
}
</style>
