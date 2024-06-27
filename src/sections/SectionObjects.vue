<template>
  <div class="objects">
    <div class="lw-container objects__container">
      <div class="sort">
        <div class="lw-select">
          <select class="custom-select">
            <option value="Срок сдачи">Срок сдачи</option>
            <option value="3 месяца">3 месяца</option>
            <option value="1й квартал 2039 года">1й квартал 2039 года</option>
            <option value="3 месяца">3 месяца</option>
            <option value="1й квартал 2039 года">1й квартал 2039 года</option>
            <option value="3 месяца">3 месяца</option>
            <option value="1й квартал 2039 года">1й квартал 2039 года</option>
            <option value="3 месяца">3 месяца</option>
            <option value="1й квартал 2039 года">1й квартал 2039 года</option>
            <option value="3 месяца">3 месяца</option>
            <option value="1й квартал 2039 года">1й квартал 2039 года</option>
          </select>
        </div>
        <div class="lw-main-input-wrapper">
          <span>Цена:</span>
          <input type="text" placeholder="от" />
          <input type="text" placeholder="до" />
        </div>
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
        <button class="lw-main-btn" type="button">
          <span>Подобрать</span>
        </button>
      </div>
      <div class="objects__header">
        <span class="lw-text lw-text--md">Для вас подобрано 120 объектов</span>
        <button
          class="lw-simple-btn lw-simple-btn--success-color ymaps-opener"
          type="button"
        >
          <img
            src="assets/img/icon-map.svg"
            alt="Посмотреть"
            width="24"
            height="24"
          /><span>Посмотреть на карте</span>
        </button>
      </div>
      <div class="objects__map">
        <div
          id="yMaps"
          data-center="59.90297506420561, 30.39827949999997"
          data-coords="59.90297506420561, 30.39827949999997"
          data-img="assets/img/object-2.jpg"
          data-link="object-detail.html"
          data-objects='[{"type":"1 кк","value":"1305"},{"type":"2 кк","value":"105"},{"type":"3 кк","value":"506"},{"type":"4 кк","value":"608"},{"type":"5 кк","value":"7"}]'
        ></div>
      </div>
      <div class="objects__grid">
        <div class="object-preview-card">
          <div class="object-preview-card__header">
            <img
              class="lw-no-image"
              src="assets/img/icon-no-image.svg"
              alt="Объект"
              width="100"
              height="100"
            />
          </div>
          <div class="object-preview-card__content">
            <span class="lw-text lw-text--md lw-text--semi"
              >Просторный ЖК бизнес-класса “Белые ночи”</span
            ><small class="lw-text lw-text--light">Чкаловский район</small
            ><span class="lw-text"
              >г. Москва, просп. Центральный проезд Хорошевского Серебряного
              Бора</span
            >
            <div class="object-station">
              <ul class="object-station-list">
                <li class="object-station-list-item">
                  <div class="object-station-list-item-side">
                    <img
                      src="assets/img/icon-metro.svg"
                      alt="Волгоградский проспект"
                      width="18"
                      height="18"
                    /><span class="lw-text lw-text--semi"
                      >Волгоградский проспект</span
                    >
                  </div>
                  <div class="object-station-list-item-side">
                    <span class="lw-text lw-text--light">20 мин</span
                    ><img
                      src="assets/img/icon-man.svg"
                      alt="пешком"
                      width="14"
                      height="14"
                    />
                  </div>
                </li>
                <li class="object-station-list-item">
                  <div class="object-station-list-item-side">
                    <img
                      src="assets/img/icon-metro.svg"
                      alt="Волгоградский проспект"
                      width="18"
                      height="18"
                    /><span class="lw-text lw-text--semi"
                      >Волгоградский проспект</span
                    >
                  </div>
                  <div class="object-station-list-item-side">
                    <span class="lw-text lw-text--light">20 мин</span
                    ><img
                      src="assets/img/icon-man.svg"
                      alt="пешком"
                      width="14"
                      height="14"
                    />
                  </div>
                </li>
                <li
                  class="object-station-list-item object-station-list-item--hidden"
                >
                  <div class="object-station-list-item-side">
                    <img
                      src="assets/img/icon-metro.svg"
                      alt="Волгоградский проспект"
                      width="18"
                      height="18"
                    /><span class="lw-text lw-text--semi"
                      >Волгоградский проспект</span
                    >
                  </div>
                  <div class="object-station-list-item-side">
                    <span class="lw-text lw-text--light">20 мин</span
                    ><img
                      src="assets/img/icon-man.svg"
                      alt="пешком"
                      width="14"
                      height="14"
                    />
                  </div>
                </li>
              </ul>
              <button
                class="lw-simple-btn lw-simple-btn--success-color object-station-list-btn"
                type="button"
              >
                <span>Показать еще...</span>
              </button>
            </div>
            <table>
              <thead>
                <tr>
                  <td>Найдено:</td>
                  <td>Кол-во:</td>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td>Студия от 3.44 млн руб.</td>
                  <td><a href="#">13</a></td>
                </tr>
                <tr>
                  <td>1 кк от 244.24 млн руб</td>
                  <td><a href="#">13 000</a></td>
                </tr>
              </tbody>
            </table>
            <a
              class="lw-main-btn lw-main-btn--outlined object-preview-card__detail-link"
              href="object-detail.html"
              ><span>Квартиры</span></a
            >
          </div>
        </div>
        <div class="object-preview-card">
          <div class="object-preview-card__header">
            <img
              src="assets/img/object-2.jpg"
              alt="Объект"
              width="360"
              height="220"
            />
          </div>
          <div class="object-preview-card__content">
            <span class="lw-text lw-text--md lw-text--semi"
              >Просторный ЖК бизнес-класса “Белые ночи”</span
            ><small class="lw-text lw-text--light">Чкаловский район</small
            ><span class="lw-text"
              >г. Москва, просп. Центральный проезд Хорошевского Серебряного
              Бора</span
            >
            <div class="object-station">
              <ul class="object-station-list">
                <li class="object-station-list-item">
                  <div class="object-station-list-item-side">
                    <img
                      src="assets/img/icon-metro.svg"
                      alt="Волгоградский проспект"
                      width="18"
                      height="18"
                    /><span class="lw-text lw-text--semi"
                      >Волгоградский проспект</span
                    >
                  </div>
                  <div class="object-station-list-item-side">
                    <span class="lw-text lw-text--light">20 мин</span
                    ><img
                      src="assets/img/icon-man.svg"
                      alt="пешком"
                      width="14"
                      height="14"
                    />
                  </div>
                </li>
                <li class="object-station-list-item">
                  <div class="object-station-list-item-side">
                    <img
                      src="assets/img/icon-metro.svg"
                      alt="Волгоградский проспект"
                      width="18"
                      height="18"
                    /><span class="lw-text lw-text--semi"
                      >Волгоградский проспект</span
                    >
                  </div>
                  <div class="object-station-list-item-side">
                    <span class="lw-text lw-text--light">20 мин</span
                    ><img
                      src="assets/img/icon-man.svg"
                      alt="пешком"
                      width="14"
                      height="14"
                    />
                  </div>
                </li>
                <li
                  class="object-station-list-item object-station-list-item--hidden"
                >
                  <div class="object-station-list-item-side">
                    <img
                      src="assets/img/icon-metro.svg"
                      alt="Волгоградский проспект"
                      width="18"
                      height="18"
                    /><span class="lw-text lw-text--semi"
                      >Волгоградский проспект</span
                    >
                  </div>
                  <div class="object-station-list-item-side">
                    <span class="lw-text lw-text--light">20 мин</span
                    ><img
                      src="assets/img/icon-man.svg"
                      alt="пешком"
                      width="14"
                      height="14"
                    />
                  </div>
                </li>
                <li
                  class="object-station-list-item object-station-list-item--hidden"
                >
                  <div class="object-station-list-item-side">
                    <img
                      src="assets/img/icon-metro.svg"
                      alt="Волгоградский проспект"
                      width="18"
                      height="18"
                    /><span class="lw-text lw-text--semi"
                      >Волгоградский проспект</span
                    >
                  </div>
                  <div class="object-station-list-item-side">
                    <span class="lw-text lw-text--light">20 мин</span
                    ><img
                      src="assets/img/icon-man.svg"
                      alt="пешком"
                      width="14"
                      height="14"
                    />
                  </div>
                </li>
                <li
                  class="object-station-list-item object-station-list-item--hidden"
                >
                  <div class="object-station-list-item-side">
                    <img
                      src="assets/img/icon-metro.svg"
                      alt="Волгоградский проспект"
                      width="18"
                      height="18"
                    /><span class="lw-text lw-text--semi"
                      >Волгоградский проспект</span
                    >
                  </div>
                  <div class="object-station-list-item-side">
                    <span class="lw-text lw-text--light">20 мин</span
                    ><img
                      src="assets/img/icon-man.svg"
                      alt="пешком"
                      width="14"
                      height="14"
                    />
                  </div>
                </li>
                <li
                  class="object-station-list-item object-station-list-item--hidden"
                >
                  <div class="object-station-list-item-side">
                    <img
                      src="assets/img/icon-metro.svg"
                      alt="Волгоградский проспект"
                      width="18"
                      height="18"
                    /><span class="lw-text lw-text--semi"
                      >Волгоградский проспект</span
                    >
                  </div>
                  <div class="object-station-list-item-side">
                    <span class="lw-text lw-text--light">20 мин</span
                    ><img
                      src="assets/img/icon-man.svg"
                      alt="пешком"
                      width="14"
                      height="14"
                    />
                  </div>
                </li>
              </ul>
              <button
                class="lw-simple-btn lw-simple-btn--success-color object-station-list-btn"
                type="button"
              >
                <span>Показать еще...</span>
              </button>
            </div>
            <table>
              <thead>
                <tr>
                  <td>Найдено:</td>
                  <td>Кол-во:</td>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td>Студия от 3.44 млн руб.</td>
                  <td><a href="#">13</a></td>
                </tr>
                <tr>
                  <td>1 кк от 244.24 млн руб</td>
                  <td><a href="#">13 000</a></td>
                </tr>
              </tbody>
            </table>
            <a
              class="lw-main-btn lw-main-btn--outlined object-preview-card__detail-link"
              href="object-detail.html"
              ><span>Квартиры</span></a
            >
          </div>
        </div>
        <div class="object-preview-card">
          <div class="object-preview-card__header">
            <img
              src="assets/img/object-1.jpg"
              alt="Объект"
              width="360"
              height="220"
            />
          </div>
          <div class="object-preview-card__content">
            <span class="lw-text lw-text--md lw-text--semi"
              >Просторный ЖК бизнес-класса “Белые ночи”</span
            ><small class="lw-text lw-text--light">Чкаловский район</small
            ><span class="lw-text"
              >г. Москва, просп. Центральный проезд Хорошевского Серебряного
              Бора</span
            >
            <div class="object-station">
              <ul class="object-station-list">
                <li class="object-station-list-item">
                  <div class="object-station-list-item-side">
                    <img
                      src="assets/img/icon-metro.svg"
                      alt="Волгоградский проспект"
                      width="18"
                      height="18"
                    /><span class="lw-text lw-text--semi"
                      >Волгоградский проспект</span
                    >
                  </div>
                  <div class="object-station-list-item-side">
                    <span class="lw-text lw-text--light">20 мин</span
                    ><img
                      src="assets/img/icon-man.svg"
                      alt="пешком"
                      width="14"
                      height="14"
                    />
                  </div>
                </li>
              </ul>
            </div>
            <table>
              <thead>
                <tr>
                  <td>Найдено:</td>
                  <td>Кол-во:</td>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td>Студия от 3.44 млн руб.</td>
                  <td><a href="#">13</a></td>
                </tr>
                <tr>
                  <td>1 кк от 244.24 млн руб</td>
                  <td><a href="#">13 000</a></td>
                </tr>
              </tbody>
            </table>
            <a
              class="lw-main-btn lw-main-btn--outlined object-preview-card__detail-link"
              href="object-detail.html"
              ><span>Квартиры</span></a
            >
          </div>
        </div>
        <div class="object-preview-card">
          <div class="object-preview-card__header">
            <img
              src="assets/img/object-2.jpg"
              alt="Объект"
              width="360"
              height="220"
            />
          </div>
          <div class="object-preview-card__content">
            <span class="lw-text lw-text--md lw-text--semi"
              >Просторный ЖК бизнес-класса “Белые ночи”</span
            ><small class="lw-text lw-text--light">Чкаловский район</small
            ><span class="lw-text"
              >г. Москва, просп. Центральный проезд Хорошевского Серебряного
              Бора</span
            >
            <div class="object-station">
              <ul class="object-station-list">
                <li class="object-station-list-item">
                  <div class="object-station-list-item-side">
                    <img
                      src="assets/img/icon-metro.svg"
                      alt="Волгоградский проспект"
                      width="18"
                      height="18"
                    /><span class="lw-text lw-text--semi"
                      >Волгоградский проспект</span
                    >
                  </div>
                  <div class="object-station-list-item-side">
                    <span class="lw-text lw-text--light">20 мин</span
                    ><img
                      src="assets/img/icon-man.svg"
                      alt="пешком"
                      width="14"
                      height="14"
                    />
                  </div>
                </li>
                <li class="object-station-list-item">
                  <div class="object-station-list-item-side">
                    <img
                      src="assets/img/icon-metro.svg"
                      alt="Волгоградский проспект"
                      width="18"
                      height="18"
                    /><span class="lw-text lw-text--semi"
                      >Волгоградский проспект</span
                    >
                  </div>
                  <div class="object-station-list-item-side">
                    <span class="lw-text lw-text--light">20 мин</span
                    ><img
                      src="assets/img/icon-man.svg"
                      alt="пешком"
                      width="14"
                      height="14"
                    />
                  </div>
                </li>
                <li
                  class="object-station-list-item object-station-list-item--hidden"
                >
                  <div class="object-station-list-item-side">
                    <img
                      src="assets/img/icon-metro.svg"
                      alt="Волгоградский проспект"
                      width="18"
                      height="18"
                    /><span class="lw-text lw-text--semi"
                      >Волгоградский проспект</span
                    >
                  </div>
                  <div class="object-station-list-item-side">
                    <span class="lw-text lw-text--light">20 мин</span
                    ><img
                      src="assets/img/icon-man.svg"
                      alt="пешком"
                      width="14"
                      height="14"
                    />
                  </div>
                </li>
              </ul>
              <button
                class="lw-simple-btn lw-simple-btn--success-color object-station-list-btn"
                type="button"
              >
                <span>Показать еще...</span>
              </button>
            </div>
            <table>
              <thead>
                <tr>
                  <td>Найдено:</td>
                  <td>Кол-во:</td>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td>Студия от 3.44 млн руб.</td>
                  <td><a href="#">13</a></td>
                </tr>
                <tr>
                  <td>1 кк от 244.24 млн руб</td>
                  <td><a href="#">13 000</a></td>
                </tr>
              </tbody>
            </table>
            <a
              class="lw-main-btn lw-main-btn--outlined object-preview-card__detail-link"
              href="object-detail.html"
              ><span>Квартиры</span></a
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// import SortComponent from "@/components/SortComponent.vue";
// import LwBtn from "@/mixins/LwBtn.vue";
// import ObjectPreviewCard from "@/mixins/ObjectPreviewCard.vue";

export default {
  // components: {
  //   SortComponent,
  //   LwBtn,
  //   ObjectPreviewCard,
  // },
  data() {
    return {
      cards: [
        {
          img: "object-2.jpg",
          title: "Просторный ЖК бизнес-класса “Белые ночи”",
          small: "Чкаловский район",
          address:
            "г. Москва, просп. Центральный проезд Хорошевского Серебряного Бора",
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
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/mixins";
@import "@/styles/extends";
.objects {
  .sort {
    margin-bottom: var(--main-offset);
  }

  &__map {
    margin-bottom: var(--main-offset);
    border-radius: 10px;
    overflow: hidden;
    display: none;

    &.is-open {
      display: block;
    }
  }

  &__header {
    display: flex;
    align-items: center;
    gap: 30px;
    margin-bottom: var(--main-offset);

    @include m-b-mobile-lg-down {
      flex-direction: column;
      align-items: flex-start;
      gap: 12px;
    }
  }

  &__grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: clamp(20px, 2vw, 30px);

    @include m-b-down(860px) {
      grid-template-columns: repeat(2, 1fr);
    }

    @include m-b-down(600px) {
      grid-template-columns: 1fr;
    }
  }
}
</style>
