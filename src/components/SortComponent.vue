<template>
  <div class="sort">
    <LwSelect :options="sortOptions" />
    <LwMainInput />
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
    <button class="lw-main-btn" type="button"><span>Подобрать</span></button>
  </div>
</template>

<script>
import LwSelect from "@/mixins/LwSelect.vue";
import LwMainInput from "@/mixins/LwMainInput.vue";
// import LwMultipleChecker from "./LwMultipleChecker.vue";

export default {
  name: "SortComponent",
  components: {
    LwMainInput,
    LwSelect,
    // LwMultipleChecker,
  },
  data() {
    return {
      sortOptions: [
        "Срок сдачи",
        "3 месяца",
        "1й квартал 2039 года",
        "3 месяца",
        "1й квартал 2039 года",
        "3 месяца",
        "1й квартал 2039 года",
        "3 месяца",
        "1й квартал 2039 года",
        "3 месяца",
        "1й квартал 2039 года",
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/mixins";
.sort {
  display: flex;
  flex-wrap: wrap;
  align-items: flex-start;
  gap: 20px;

  & > * {
    width: calc(25% - 20px);

    min-height: 40px;
  }

  .custom-select-opener {
    min-height: 40px;
  }

  @include m-b-down(1140px) {
    & > * {
      width: calc(50% - 10px);
    }
  }

  @include m-b-down(620px) {
    & > * {
      width: 100%;
    }
  }
}
</style>
