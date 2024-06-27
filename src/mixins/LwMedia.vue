<template>
  <div class="lw-media">
    <div class="lw-media__grid">
      <template v-if="photos">
        <div
          v-for="photo in photos"
          :key="photo.id"
          :class="{ 'is-cover': photo.isCover }"
          class="lw-media__grid-item"
        >
          <img
            :src="require(`@/assets/img/${photo.img}`)"
            alt="Описание фото"
            width="180"
            height="180"
          />
          <div v-if="photo.isChecker">
            <input type="checkbox" :checked="photo.isChecked" :id="photo.id" />
            <label :for="photo.id" aria-label="Выбрать фото"></label>
          </div>
        </div>
      </template>

      <div class="lw-media__grid-item">
        <button
          type="button"
          aria-label="Добавить"
          class="lw-main-btn lw-main-btn--media"
        >
          <img
            src="@/assets/img/icon-add-media.svg"
            alt="Описание фото"
            width="180"
            height="180"
          />
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "LwMedia",
  props: {
    photos: Array,
  },
};
</script>

<style lang="scss" scoped>
:root {
  --lw-media-border-color: transparent;
  --lw-media-is-cover-border-color: #4caf50;
}

.lw-media {
  width: 100%;
  max-width: 800px;

  &__grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 20px;

    @media (max-width: 534px) {
      grid-template-columns: repeat(2, 1fr);
      gap: 10px;
    }
  }

  &__grid-item {
    position: relative;
    border-radius: 6px;
    overflow: hidden;
    aspect-ratio: 1 / 1;

    input {
      display: none;
    }

    input:checked + label {
      background-color: #4caf50;

      background-image: url("@/assets/img/icon-check.svg");
      background-repeat: no-repeat;
      background-position: center;
    }

    label {
      position: absolute;
      top: 10px;
      left: 10px;
      width: 20px;
      height: 20px;
      background-color: #ffffff;
      border: 2px solid #dedede;
      border-radius: 3px;

      cursor: pointer;
    }

    &.is-cover {
      border: 1px solid var(--lw-media-is-cover-border-color);

      &::before {
        position: absolute;
        bottom: 0;
        left: 0;
        content: "Обложка";
        width: fit-content;
        height: fit-content;
        font-size: 12px;
        font-weight: 400;
        background-color: green;
        color: white;
        padding: 6px 12px;
        border-radius: 0 6px 0 0;
      }
    }

    img {
      display: block;
      width: 100%;
      height: auto;
      aspect-ratio: 1/1;
      object-fit: cover;
    }
  }
}
</style>
