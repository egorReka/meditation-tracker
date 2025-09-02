<script setup lang="ts">
import IconArrow from '@/icons/IconArrow.vue';
import { useMeditationsStore } from '@/stores/meditations.store';
import { onMounted } from 'vue';

const store = useMeditationsStore();

onMounted(() => {
  store.fetchMeditations();
})
</script>

<template>
  <ul class="meditation-list">
    <li v-for="meditation in store.meditations" :key="meditation.id">
      <div class="meditation-card">
        <div class="meditation-card__content">
          <h3 class="meditation-card__title">{{ meditation.title }}</h3>
          <p class="meditation-card__description">{{ meditation.description }}</p>
        </div>

        <div class="meditation-card__wrapper">
          <button class="meditation-card__button">
            Начать
            <IconArrow />
          </button>

          <span class="meditation-card__time">{{ `${meditation.duration_min} мин` }}</span>
        </div>

      </div>
    </li>
  </ul>
</template>

<style scope>
.meditation-list {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 22px;
  list-style: none;
  margin: 0;
  padding: 0;
}

.meditation-card {
  display: grid;
  grid-template-rows: 1fr auto;
  gap: 15px;
  width: 100%;
  height: 100%;
  padding: 22px 30px;
  font-weight: 500;
  color: var(--color-default-black);
  background-color: var(--color-hint-of-red);
  border-radius: 20px;
}

.meditation-card__title {
  margin: 0;
  font-size: 25px;
  font-weight: 700;
}

.meditation-card__description {
  margin: 0;
  font-size: 15px;
}

.meditation-card__wrapper {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  gap: 10px;
}

.meditation-card__button {
  display: flex;
  align-items: center;
  gap: 11px;
  padding: 10px 17px;
  border-radius: 10px;
  font-weight: 500;
  font-size: 15px;
  line-height: 120%;
  color: var(--color-default-white);
  background-color: var(--color-swamp);
  border: none;
  cursor: pointer;
  transition: opacity 0.2s;
}

.meditation-card__button:hover {
  opacity: 0.9;
}

.meditation-card__time {
  font-weight: 500;
  font-size: 15px;
  color: var(--color-swamp);
  opacity: 0.75;
}
</style>
