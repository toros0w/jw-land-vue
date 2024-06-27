<template>
  <div class="object-detail-map">
    <div class="lw-container">
      <ObjectCard v-bind="objectCardProps" />
    </div>
  </div>
  <div class="object-detail">
    <div class="lw-container object-detail__container">
      <span class="lw-text lw-text--md lw-text--bold">Описание ЖК</span>
      <div class="object-detail__main">
        <LwMainSlider :slides="sliders" />
        <div class="object-detail__info">
          <span class="lw-text lw-text--md lw-text--semi"
            >Просторный ЖК бизнес-класса “Белые ночи” у Пресненской
            набережной</span
          >
          <LwBtn
            cls="lw-simple-btn lw-simple-btn--success-color collapsed-block-opener"
            tag="button"
            text="Подробнее"
            icon="icon-arr-d-green.svg"
            iconSide="right"
            iconAlt="Подробнее"
          />
          <div class="collapsed-block">
            <small class="lw-text lw-text--light"
              >Чкаловский Нагатинская набережная Судостроительной улицы
              район</small
            ><span class="lw-text"
              >г. Москва, просп. Центральный проезд Хорошевского Серебряного
              Бора, д.1455550, стр. 145, д. 123, к. 1234</span
            >
            <div class="object-station">
              <ObjectStationList :stations="stations" />
              <button
                class="lw-simple-btn lw-simple-btn--success-color object-station-list-btn"
                type="button"
              >
                <span>Показать еще...</span>
              </button>
            </div>
            <div class="object-detail__chars">
              <LwSimpleTable :tbody="charsTable.tbody" />
            </div>
          </div>
        </div>
      </div>
      <div class="object-detail__desc">
        <p class="lw-text lw-text--light lw-text-truncate truncated">
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
          <br />
          <br />
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
        <button
          class="lw-simple-btn lw-simple-btn--success-color text-expand-btn"
          type="button"
        >
          <span>Читать далее...</span>
        </button>
      </div>
      <div class="object-detail__map">
        <iframe
          src="https://yandex.ru/map-widget/v1/?um=constructor%3A0bf5ace7c58a15845578e7fe1e46fd0e19af91d80973dca246c4487c4e29b8ee&amp;source=constructor"
          width="900"
          height="400"
        ></iframe>
      </div>
    </div>
  </div>
</template>

<script>
import LwMainSlider from "@/mixins/LwMainSlider.vue";
import LwBtn from "@/mixins/LwBtn.vue";
import LwSimpleTable from "@/mixins/LwSimpleTable.vue";
import ObjectStationList from "@/mixins/ObjectStationList.vue";
import ObjectCard from "@/mixins/ObjectCard.vue";
export default {
  components: {
    LwMainSlider,
    LwBtn,
    ObjectCard,
    ObjectStationList,
    LwSimpleTable,
  },
  data() {
    return {
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
    };
  },
};
</script>

<style scoped></style>
