<script setup lang="ts">
import ButtonFeel from './ButtonFeel.vue';
import IconRelax from '@/icons/IconRelax.vue';
import IconCalm from '@/icons/IconCalm.vue';
import IconFocus from '@/icons/IconFocus.vue';
import IconAnxious from '@/icons/IconAnxious.vue';
</script>
<template>

  <div class="profile">
    <img class="profile__img" src="../assets/img/avatar.jpg" alt="avatar">
    <h2 class="profile__title">Добро пожаловать, Наталья!</h2>
    <p class="profile__text">Как вы сегодня себя чувствуете?</p>

    <ul class="profile__list">
      <li class="profile__item">
        <ButtonFeel>
          <template #icon>
            <IconCalm />
          </template>

          спокойно
        </ButtonFeel>
      </li>

      <li class="profile__item">
        <ButtonFeel>
          <template #icon>
            <IconRelax />
          </template>

          Расслабленно
        </ButtonFeel>
      </li>

      <li class="profile__item">
        <ButtonFeel>
          <template #icon>
            <IconFocus />
          </template>

          Фокусировано
        </ButtonFeel>
      </li>

      <li class="profile__item">
        <ButtonFeel>
          <template #icon>
            <IconAnxious />
          </template>

          Тревожно
        </ButtonFeel>
      </li>
    </ul>
  </div>

</template>
<style scope>
.profile {
  min-width: 370px;
  padding-top: 23px;
}

.profile__img {
  width: 129px;
  height: 129px;
  margin-bottom: 30px;
  border-radius: 50%;
}

.profile__title {
  font-weight: 500;
  font-size: 30px;
}

.profile__text {
  margin-bottom: 39px;
  font-size: 22px;
  opacity: 0.7;
}

.profile__list {
  display: grid;
  grid-template-columns: repeat(4, auto);
  gap: 12px;
  max-width: 325px;
  list-style: none;
  margin: 0;
  padding: 0;
}
</style>
