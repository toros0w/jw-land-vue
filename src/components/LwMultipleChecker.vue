<template>
  <div class="lw-multiple-checker">
    <div class="lw-multiple-checker-panel"><span>Тип квартиры</span></div>
    <div class="lw-multiple-checker-container">
      <input type="checkbox" id="lw_m_1" checked="checked" />
      <label for="lw_m_1">Студия</label>
      <input type="checkbox" id="lw_m_2" />
      <label for="lw_m_2">1к.кв.</label>
      <input type="checkbox" id="lw_m_3" checked="checked" />
      <label for="lw_m_3">2к.кв.</label>
      <input type="checkbox" id="lw_m_4" />
      <label for="lw_m_4">3к.кв.</label>
      <input type="checkbox" id="lw_m_5" checked="checked" />
      <label for="lw_m_5">4к.кв.</label>
      <input type="checkbox" id="lw_m_6" checked="checked" />
      <label for="lw_m_6">5к.кв.</label>
      <input type="checkbox" id="lw_m_7" checked="checked" />
      <label for="lw_m_7">6+к.кв.</label>
    </div>
  </div>
</template>

<script>
export default {
  name: "LwMultipleChecker",
};
</script>

<style lang="scss" scoped>
.lw-multiple-checker {
  position: relative;

  &-panel {
    display: flex;
    align-items: center;
    gap: 8px;

    min-height: 40px;
    padding: 8px 16px;
    padding-right: 50px;
    cursor: pointer;
    box-shadow: 0px 4px 14px rgba(0, 0, 0, 0.04);

    span {
      font-size: 14px;
      white-space: nowrap;
      text-overflow: ellipsis;
      width: 100%;
      display: block;
      overflow: hidden;
      line-height: 1;
      color: #333333;
    }

    &::after {
      position: absolute;
      top: 11px;
      right: 16px;
      content: "";
      width: 16px;
      height: 16px;
      background-image: url("@/assets/img/icon-arrow-down.svg");
      background-repeat: no-repeat;
      background-size: 16px;
      background-position: center;
      transition: transform var(--main-transition);
    }

    &.is-open {
      &::after {
        transform: rotate(180deg);
      }
    }
  }

  &-container {
    position: absolute;

    top: calc(100% + 2px);
    left: 0;

    width: 100%;
    padding: 10px 16px;

    border-radius: 3px;
    background-color: #ffffff;
    z-index: 10;

    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    visibility: hidden;
    opacity: 0;

    input {
      display: none;
    }

    label {
      font-size: 14px;
      font-weight: 400;
      color: #333333;
      white-space: nowrap;
      background-color: #dedede;
      cursor: pointer;

      border-radius: 3px;
      padding: 8px 10px;

      overflow: hidden;
      text-overflow: ellipsis;
      max-width: 160px;

      transition: all 0.1s ease-in;
    }

    @media (hover: hover) {
      label:hover,
      label:focus {
        color: #ffffff;
        background-color: #4caf50;
      }
    }

    input:checked + label {
      color: #ffffff;
      background-color: #4caf50;
    }
  }

  &-panel.is-open + .lw-multiple-checker-container {
    visibility: visible;
    opacity: 1;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;
  }
}
</style>
