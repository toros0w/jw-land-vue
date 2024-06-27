<template>
  <div class="user">
    <img
      class="user-avatar"
      src="assets/img/user-avatar.png"
      alt="Аватар"
      width="60"
      height="60"
    />
    <div class="user-content">
      <span class="lw-text lw-text--sm"
        >Ваш менеджер
        <span class="user-name">Константинов Константин</span></span
      ><span class="user-phone lw-text lw-text--sm lw-text--light"
        >Телефон: <a href="tel:+79999999999">+7 (999) 999 99 99</a></span
      ><span class="user-mail lw-text lw-text--sm lw-text--light"
        >Почта: <a href="mailto:info-email@mail.ru">info-email@mail.ru</a></span
      >
    </div>
  </div>
</template>

<script></script>

<style lang="scss" scoped>
@import "@/styles/extends";
.user {
  display: flex;
  align-items: center;
  gap: 10px;

  &-avatar {
    width: 60px;
    height: 60px;
  }

  &-name {
  }

  &-mail,
  &-phone {
    a {
      color: var(--success);
    }
  }

  &-content {
    @extend .flex-column;
    gap: 5px;
  }
}
</style>
