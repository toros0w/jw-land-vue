<template>
  <section class="lw-section">
    <div class="lw-container lw-section-container">
      <span class="lw-title">{{ data.title }}</span>
      <div v-if="data.sectionRows">
        <div
          v-for="row in data.sectionRows"
          :key="row"
          :class="['lw-section-row', row.modifier]"
        >
          <span v-if="row.title" class="lw-title">
            {{ row.title }}
            <span v-if="row.titleNote"> {{ row.titleNote }}</span>
          </span>
          <div v-if="row.cols == 2">
            <div :class="['lw-section-row-col', row.colModifier]">
              <div v-for="group in row.controlGroups" :key="group">
                <LwControlGroup
                  v-for="ctrls in group.controlsGroup"
                  :key="ctrls"
                  :data="ctrls"
                  :modifier="group.modifier"
                />
              </div>
            </div>
            <div :class="['lw-section-row-col', row.col2Modifier]">
              <div v-for="group in row.controlGroups2" :key="group">
                <LwControlGroup
                  v-for="ctrls in group.controlsGroup"
                  :key="ctrls"
                  :data="ctrls"
                  :modifier="group.modifier"
                />
              </div>
            </div>
          </div>
          <div v-else>
            <div v-for="group in row.controlGroups" :key="group">
              <LwControlGroup
                v-for="ctrls in group.controlsGroup"
                :key="ctrls"
                :data="ctrls"
                :modifier="group.modifier"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import LwControlGroup from "./LwControlGroup.vue";

export default {
  name: "MainSection",
  components: {
    LwControlGroup,
  },
  props: {
    data: Object,
  },
};
</script>

<style scoped></style>
