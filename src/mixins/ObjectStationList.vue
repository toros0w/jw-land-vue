<template>
  <div class="object-station">
    <ul class="object-station-list">
      <li
        v-for="(station, index) in stations"
        :key="station.name"
        :class="{ 'object-station-list-item--hidden': index > 1 }"
        class="object-station-list-item"
      >
        <div class="object-station-list-item-side">
          <img
            src="assets/img/icon-metro.svg"
            :alt="station.name"
            width="18"
            height="18"
          />
          <span class="lw-text lw-text--semi">{{ station.name }}</span>
        </div>
        <div class="object-station-list-item-side">
          <span class="lw-text lw-text--light">{{
            station.ambulationTime
          }}</span>
          <img
            :src="`assets/img/${station.ambulationTypeIcon}`"
            :alt="station.ambulationTypeName"
            :width="station.ambulationTypeIconWidth"
            :height="station.ambulationTypeIconHeight"
          />
        </div>
      </li>
    </ul>
    <LwBtn
      v-if="stations.length > 2"
      :cls="'lw-simple-btn lw-simple-btn--success-color object-station-list-btn'"
      :tag="'button'"
      :text="'Показать еще...'"
    />
  </div>
</template>

<script>
import LwBtn from "./LwBtn.vue";

export default {
  name: "ObjectStationList",
  components: {
    LwBtn,
  },
  props: {
    stations: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/extends";
@import "@/styles/mixins";

.object-station {
  @extend .flex-column;
  gap: 10px;

  &-list {
    @extend .list-reset;

    &-item {
      display: flex;
      align-items: center;
      gap: 20px;

      &:not(:last-child) {
        margin-bottom: 10px;
      }

      &-side {
        display: flex;
        align-items: center;
        gap: 5px;
        min-width: 75px;

        img {
          height: 14px;
          width: auto;
          object-fit: contain;
        }
      }

      &--hidden {
        display: none;
      }
    }

    &-btn {
      width: fit-content;
    }
  }
}
.objects-list {
  &--table-view {
    @include m-b-laptop-down {
      display: none;
    }

    table {
      width: 100%;
      min-width: 1140px;

      tr {
        height: 40px;
        border-bottom: 1px solid #dedede;
      }

      td {
        text-align: center;
        padding: 12px 16px;

        a {
          color: inherit;
        }

        img {
          min-width: 24px;
        }
      }
    }
  }

  &--card-view {
    display: none;

    @include m-b-laptop-down {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 20px;
    }

    @include m-b-mobile-lg-down {
      grid-template-columns: 1fr;
    }

    .object-card {
      grid-template-columns: 1fr;
      gap: 0;
      border: var(--main-border);
      border-radius: 5px;

      &__img {
        border-radius: 0;
        border: none;
        border-bottom: var(--main-border);

        .lw-fv-btn {
          display: flex;
        }
      }

      &__info {
        padding: 20px;
        padding-bottom: 10px;

        position: static;
        top: 0;

        table {
          tr:first-child td {
            padding-top: 5px;
          }

          td:last-child {
            text-align: right;
          }
        }
      }

      .lw-main-btn {
        grid-column: initial;
        margin: 20px;
        margin-top: 10px;
        width: calc(100% - 40px);
      }
    }
  }
}
</style>
