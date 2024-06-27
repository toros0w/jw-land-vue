<template>
  <div class="object-detail">
    <div class="lw-container object-detail__container">
      <div class="object-detail__main">
        <LwMainSlider :slides="sliders" />
        <div class="object-detail__info">
          <div class="object-detail__info-top">
            <LwBtn
              cls="lw-simple-btn lw-simple-btn--success-color"
              tag="a"
              href="object-detail-map.html"
              text="На карте"
              icon="icon-map.svg"
              :iconWidth="24"
              :iconHeight="24"
              iconAlt="На карт"
            />
            <LwFvBtn :state="false" text="test" />
          </div>
          <span class="lw-text lw-text--md lw-text--semi"
            >Просторный ЖК бизнес-класса “Белые ночи” у Пресненской
            набережной</span
          ><small class="lw-text lw-text--light"
            >Чкаловский Нагатинская набережная Судостроительной улицы
            район</small
          ><span class="lw-text"
            >г. Москва, просп. Центральный проезд Хорошевского Серебряного Бора,
            д.1455550, стр. 145, д. 123, к. 1234</span
          >
          <ObjectStationList :stations="stations" />
          <div class="object-detail__chars">
            <LwSimpleTable :tbody="charsTable.tbody" />
          </div>
        </div>
      </div>
      <div class="object-detail__desc">
        <span class="lw-text lw-text--md lw-text--bold object-detail__title"
          >Описание ЖК</span
        >
        <p class="lw-text lw-text--light">
          Идею сочетания городской застройки с общественными зданиями и
          предприятиями социального назначения начали внедрять давно, но лишь
          появление жилых комплексов позволило приблизить многие услуги к людям.
          <br />
          В идеале итогом строительства жилых комплексов становится оптимальное
          сочетание жилых помещений (квартир) и нежилых площадей,
          предназначенных для комплексного бытового обслуживания их жителей.
          <br />
          Естественно, что жилые комплексы могут сильно различаться по наличию
          дополнительных услуг и уровню предоставляемого комфорта – каждый из
          них решает свою градостроительную задачу.
        </p>
      </div>
      <SortComponent />
      <ObjectCard />
      <div class="objects-list objects-list--card-view">
        <ObjectCard
          v-for="card in [1, 2, 3, 4, 5, 6]"
          :key="card"
          v-bind="objectCardProps"
        />
      </div>
      <PaginationComponent />
    </div>
  </div>
</template>

<script>
import LwFvBtn from "@/mixins/LwFvBtn.vue";
import LwMainSlider from "@/mixins/LwMainSlider.vue";
// import ImgFrame from "@/mixins/ImgFrame.vue";
import LwSimpleTable from "@/mixins/LwSimpleTable.vue";
import ObjectStationList from "@/mixins/ObjectStationList.vue";
// import LwMainSlider from "@/mixins/LwMainSlider.vue";
import ObjectCard from "@/mixins/ObjectCard.vue";
import SortComponent from "@/components/SortComponent.vue";
import PaginationComponent from "@/components/PaginationComponent.vue";

export default {
  components: {
    SortComponent,
    PaginationComponent,
    LwFvBtn,
    ObjectStationList,
    // ImgFrame,
    LwSimpleTable,
    ObjectCard,
    LwMainSlider,
  },
  data() {
    return {
      sliders: [
        {
          img: "object-slide-1.png",
        },
        {
          img: "object-slide-2.png",
        },
      ],
      stations: [
        {
          name: "Волгоградский проспект",
          ambulationTime: "20 мин",
          ambulationTypeName: "пешком",
          ambulationTypeIcon: "icon-man.svg",
          ambulationTypeIconWidth: "14",
          ambulationTypeIconHeight: "14",
        },

        {
          name: "Волгоградский проспект",
          ambulationTime: "20 мин",
          ambulationTypeName: "пешком",
          ambulationTypeIcon: "icon-man.svg",
          ambulationTypeIconWidth: "14",
          ambulationTypeIconHeight: "14",
        },

        {
          name: "Волгоградский проспект",
          ambulationTime: "20 мин",
          ambulationTypeName: "пешком",
          ambulationTypeIcon: "icon-man.svg",
          ambulationTypeIconWidth: "14",
          ambulationTypeIconHeight: "14",
        },
      ],
      charsTable: {
        tbody: {
          rows: [
            {
              tds: [
                {
                  text: "№ дома",
                },
                {
                  text: "12",
                },
              ],
            },
            {
              tds: [
                {
                  text: "Корпус",
                },
                {
                  text: "3",
                },
              ],
            },
            {
              tds: [
                {
                  text: "Этажей",
                },
                {
                  text: "25",
                },
              ],
            },
            {
              tds: [
                {
                  text: "Срок сдачи",
                },
                {
                  text: "3 квартал 2022<br>3 квартал 2022<br>3 квартал 2022",
                },
              ],
            },
          ],
        },
      },
      objectCardProps: {
        title:
          "Просторная 2-х комнатная квартира ЖК “Белые ночи” д. 13, стр. 17, кв. 29203 2-х комнатная квартира ЖК “Белые ночи” д. 13, стр. 17, кв. 29203",
        img: "object-card-img-1.png",
        moreBtn: false,

        table: {
          thead: [
            [{ value: "Стоимость" }, { value: "Стоимость кв.м." }],
            [{ value: "1 122 304 830 p." }, { value: "1 304 830 p." }],
          ],

          tbody: [
            [{ value: "Общая площадь:" }, { value: "150.68 м2" }],
            [{ value: "Корпус:" }, { value: "3" }],
            [{ value: "№ кв:" }, { value: "308" }],
            [{ value: "Тип кв:" }, { value: "2 ккв" }],
            [{ value: "Этаж:" }, { value: "10" }],
            [{ value: "Отделка:" }, { value: "Без отделки" }],
            [{ value: "Срок сдачи:" }, { value: "3 квартал 2022" }],
          ],
        },
      },
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/extends";
@import "@/styles/mixins";
.object-detail {
  &__container {
    @extend .flex-column;
    gap: var(--main-offset);
  }

  &__main {
    @extend .flex-wrap;
    gap: 20px;

    & > * {
      width: calc(50% - 20px);

      @include m-b-tablet-down {
        width: 100%;
      }
    }

    .lw-main-slider {
      position: sticky;
      top: 20px;

      @include m-b-tablet-down {
        position: static;
      }
    }
  }

  &__info {
    @extend .flex-column;
    gap: 20px;

    &-top {
      display: flex;
      align-items: center;
      gap: 20px;
      justify-content: space-between;
    }

    .collapsed-block {
      @extend .flex-column;
      gap: 20px;

      display: none;

      &.expanded {
        display: flex;
      }

      @include m-b-tablet-up {
        display: flex;
      }

      &-opener {
        width: fit-content;

        display: none;

        @include m-b-tablet-down {
          display: flex;
        }

        img {
          transform: rotate(180deg);
        }

        &.active {
          img {
            transform: rotate(0);
          }
        }

        span {
          text-decoration: initial;
        }
      }
    }
  }

  &__title {
    display: inline-block;
    margin-bottom: clamp(20px, 2vw, 30px);
  }

  &__desc {
    p:last-child {
      margin: 0;
    }

    .lw-text-truncate {
      &.truncated {
        @include text-truncate(3);
      }
    }
  }

  &__chars {
    padding-top: 10px;
    border-top: var(--main-border);
  }

  &__map {
    iframe {
      width: 100%;
      height: 50vw;
      height: 50dvw;
      max-height: 480px;
      min-height: 280px;
      border: 0;
    }
  }
}
</style>
