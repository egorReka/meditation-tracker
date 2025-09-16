<script setup lang="ts">
import ButtonAuth from '@/components/ButtonAuth.vue';
import IconLogo from '@/icons/IconLogo.vue';
</script>

<template>
  <div class="auth">
    <div class="auth__wrapper">

      <div class="auth__logo">
        <IconLogo :width="202" :height="213" />
      </div>
      <div class="auth__content">
        <h1 class="auth__title">Добро пожаловать!</h1>
        <p class="auth__text">Медитируй и оставайся в фокусе, чтобы быть счастливым.</p>
      </div>

      <ButtonAuth>
        Войти в приложение
      </ButtonAuth>

    </div>
  </div>
</template>

<style scope>
.auth {
  display: grid;
  place-content: center;
  padding: 40px 60px;
  min-height: 100svh;
  background-image: url(../assets/img/bg.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}

.auth__wrapper {
  display: grid;
  justify-items: center;
}

.auth__logo {
  margin: 0 0 39px;
}

.auth__logo svg {
  display: block;
  width: 202px;
  height: 213px;
}

.auth__content {
  margin: 0 0 64px;
  max-width: 321px;
}

.auth__title {
  margin: 0;
  font-weight: 700;
  font-size: 36px;
  text-align: center;
  line-height: 1.5;
}

.auth__text {
  margin: 0;
  font-weight: 500;
  font-size: 20px;
  text-align: center;
}
</style>
