<template>
  <div class="object-card">
    <div v-if="title" class="object-card__title">
      <span class="lw-text lw-text--md lw-text--semi">{{ title }}</span>
      <LwFvBtn :state="false" text="text" />
    </div>
    <div class="object-card__img">
      <LwFvBtn :state="false" />
      <img :src="`assets/img/${img}`" alt="Объект" width="550" height="550" />
    </div>
    <div class="object-card__info">
      <div class="lw-table-wrapper" v-if="table">
        <table>
          <thead v-if="table.thead">
            <tr v-for="tr in table.thead" :key="tr">
              <td v-for="td in tr" :key="td.value">{{ td.value }}</td>
            </tr>
          </thead>
          <tbody v-if="table.tbody">
            <tr v-for="tr in table.tbody" :key="tr">
              <td v-for="td in tr" :key="td.value">{{ td.value }}</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
    <LwBtn
      v-if="moreBtn"
      :cls="'lw-main-btn lw-main-btn--outlined'"
      :tag="'a'"
      :href="'object-detail-map.html'"
      :text="'Подробнее'"
    />
  </div>
</template>

<script>
import LwFvBtn from "./LwFvBtn.vue";
import LwBtn from "./LwBtn.vue";

export default {
  name: "ObjectCard",
  components: {
    LwFvBtn,
    LwBtn,
  },
  props: {
    title: String,
    img: String,
    table: Object,
    moreBtn: Boolean,
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/mixins";
@import "@/styles/extends";
.object-card {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: var(--main-offset);

  &__title {
    display: flex;
    gap: clamp(30px, 4vw, 60px);
    justify-content: space-between;
    grid-column: 1/3;

    @include m-b-down(675px) {
      padding-bottom: 20px;
      border-bottom: var(--main-border);
    }

    .lw-fv-btn {
      min-width: 125px;

      display: flex;

      @include m-b-tablet-down {
        display: none;
      }
    }
  }

  &__img {
    position: relative;
    height: fit-content;
    padding: 5px;

    @extend .img-frame-lg;

    .lw-fv-btn {
      position: absolute;
      top: 5px;
      right: 5px;
      display: none;

      @include m-b-tablet-down {
        display: flex;
      }
    }

    img {
      width: 100%;
      height: auto;
      object-fit: contain;
    }

    /* @include m-b-down(675px) {
      grid-row: 1/2;
      grid-column: 1/3;
    } */
  }

  &__info {
    height: fit-content;
    position: sticky;
    top: 20px;

    /* @include m-b-down(675px) {
      grid-column: 1/3; */
    /* } */

    .lw-table-wrapper {
      padding-bottom: 0;
    }

    table {
      width: 100%;
      border-collapse: collapse;

      tr {
        td {
          padding: 5px 0;
          padding-right: 10px;
          vertical-align: top;

          @include m-b-down(475px) {
            &:last-child {
              text-align: right;
            }
          }
        }
      }
      thead {
        padding-bottom: 20px;

        tr:first-child {
          td {
            padding-top: 0;
            font-weight: 400;
            color: var(--light);
          }
        }

        tr:last-child {
          td {
            font-weight: 700;
            color: var(--dark);
            padding-bottom: 20px;
            border-bottom: var(--main-border);
          }
        }
      }

      tbody {
        tr {
          &:first-child {
            td {
              padding-top: 20px;
            }
          }

          td:first-child {
            font-weight: 400;
            color: var(--light);
          }

          td:last-child {
            font-weight: 700;
            color: var(--dark);
          }
        }
      }
    }
  }

  .lw-main-btn {
    width: 100%;
    max-width: 100%;
    grid-column: 1 / 3;
  }
}
</style>
