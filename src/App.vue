<script setup lang="ts">
import MeditationList from './components/MeditationList.vue';
import UserProfile from './components/UserProfile.vue';
import IconLogo from './icons/IconLogo.vue';


</script>

<template>
  <div class="app">
    <header>
      <IconLogo />

      <nav>


      </nav>
    </header>

    <main class="main">
      <UserProfile />

      <MeditationList />
    </main>
  </div>
</template>

<style scoped>
.app {
  min-height: 100dvh;
  padding: 40px 60px;
}

.main {
  display: flex;
  justify-content: space-between;
  gap: 50px;
}
</style>
