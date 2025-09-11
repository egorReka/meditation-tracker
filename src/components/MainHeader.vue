<script setup lang="ts">
import IconPlay from '@/icons/IconPlay.vue';
import IconLogo from '../icons/IconLogo.vue';
import IconStat from '@/icons/IconStat.vue';
import IconExit from '@/icons/IconExit.vue';
</script>

<template>
  <header class="header">
    <IconLogo />

    <nav class="nav">
      <ul class="nav__list">
        <li class="nav__item">
          <RouterLink class="nav__link" to="/main" exact-active-class="is-active">
            <IconPlay />
            Медитация
          </RouterLink>
        </li>
        <li class="nav__item">
          <RouterLink class="nav__link" to="/main/stat" exact-active-class="is-active">
            <IconStat />
            Статистика
          </RouterLink>
        </li>
        <li class="nav__item">
          <RouterLink class="nav__link" to="/">
            <IconExit />
            Выход
          </RouterLink>
        </li>
      </ul>
    </nav>
  </header>

</template>
<style scope>
.header {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
}



.nav__list {
  display: flex;
  list-style: none;
  margin: 0;
  padding: 0;
}

.nav__item:not(:last-child) {
  border-right: 3px solid #3a5051;
}

.nav__link {
  padding: 20px 55px;
  display: grid;
  justify-items: center;
  transition: opacity 0.2s;
  opacity: 0.5;
}

.nav__link.is-active,
.nav__link:hover,
.nav__link:focus {
  opacity: 1;
}
</style>
