<script setup lang="ts">
import IconCloud from '@/icons/IconCloud.vue';


</script>

<template>
  <div class="stat">
    <ul class="stat__list">
      <li class="stat__item stat__item--keppel">
        <dl class="stat__card">
          <dt class="stat__header">500</dt>
          <dd class="stat__text">Минут медитации</dd>
        </dl>

        <div class="stat__icon">
          <IconCloud />
        </div>
      </li>
      <li class="stat__item stat__item--fern">
        <dl class="stat__card">
          <dt class="stat__header">10</dt>
          <dd class="stat__text">Спокойных дней</dd>
        </dl>

        <div class="stat__icon">
          <IconCloud />
        </div>
      </li>
      <li class="stat__item stat__item--shakespeare">
        <dl class="stat__card">
          <dt class="stat__header">32</dt>
          <dd class="stat__text">Расслабленных дней</dd>
        </dl>

        <div class="stat__icon">
          <IconCloud />
        </div>
      </li>
      <li class="stat__item stat__item--green-smoke">
        <dl class="stat__card">
          <dt class="stat__header">40</dt>
          <dd class="stat__text">Фокусированных дней</dd>
        </dl>

        <div class="stat__icon">
          <IconCloud />
        </div>
      </li>
      <li class="stat__item stat__item--turkish-rose">
        <dl class="stat__card">
          <dt class="stat__header">5</dt>
          <dd class="stat__text">Тревожных дней</dd>
        </dl>

        <div class="stat__icon">
          <IconCloud />
        </div>
      </li>
    </ul>
  </div>
</template>

<style scope>
.stat__list {
  display: grid;
  align-content: flex-start;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  grid-template-rows: repeat(auto-fit, minmax(200px, auto));
  gap: 50px;
  height: 100%;
  margin: 0;
  padding: 0;
  list-style: none;
}

.stat__item {
  display: grid;
  max-width: 340px;
  width: 100%;
  height: 100%;
  border-radius: 25px;
  overflow: hidden;
  background-color: var(--color-keppel);
  color: var(--color-eden);
}

.stat__item--keppel {
  background-color: var(--color-keppel);
  color: var(--color-eden);
}

.stat__item--fern {
  background-color: var(--color-fern);
  color: var(--color-parsley);
}

.stat__item--shakespeare {
  background-color: var(--color-shakespeare);
  color: var(--color-teal-blue);
}

.stat__item--green-smoke {
  background-color: var(--color-green-smoke);
  color: var(--color-saratoga);
}

.stat__item--turkish-rose {
  background-color: var(--color-turkish-rose);
  color: var(--color-jazz);
}

.stat__card {
  grid-column: 1 / -1;
  grid-row: 1 / -1;
  display: grid;
  grid-template-rows: 2fr 1fr;
  align-items: flex-end;
  gap: 35px;
  padding: 20px;
  color: var(--color-default-white);
  z-index: 1;
}

.stat__header {
  font-weight: 700;
  font-size: 80px;
  text-align: right;
  line-height: 1;
}

.stat__text {
  font-weight: 500;
  font-size: 18px;
}

.stat__icon {
  grid-column: 1 / -1;
  grid-row: 1 / -1;
  align-self: flex-end;
}

.stat__icon svg {
  display: block;
  width: 100%;
  height: auto;
  object-fit: cover;
}
</style>
