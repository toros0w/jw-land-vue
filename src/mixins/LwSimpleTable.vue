<template>
  <div class="lw-simple-table">
    <table>
      <thead v-if="thead">
        <tr v-for="row in thead.rows" :key="row">
          <td v-for="cell in row.tds" :key="cell.text" v-html="cell.text"></td>
        </tr>
      </thead>
      <tbody>
        <tr v-for="row in tbody.rows" :key="row">
          <td v-for="cell in row.tds" :key="cell.text" v-html="cell.text"></td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "LwSimpleTable",
  props: {
    thead: Object,
    tbody: Object,
  },
};
</script>

<style lang="scss" scoped>
:root {
  --lw-simple-table-left-td-color: var(--light);
  --lw-simple-table-right-td-color: var(--dark);
  --lw-simple-tble-max-width: 460px;
}

.lw-simple-table {
  width: 100%;

  table {
    width: 100%;
    max-width: var(--lw-simple-tble-max-width);
    border-collapse: collapse;

    td {
      width: 50%;
      vertical-align: top;
      padding: 10px;
      padding-left: 0;
      padding-right: 20px;

      &:first-child {
        color: var(--lw-simple-table-left-td-color);
      }

      &:last-child {
        font-weight: 700;
        color: var(--lw-simple-table-right-td-color);
      }
    }
  }
}
</style>
