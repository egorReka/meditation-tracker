<script setup lang="ts">
import MeditationList from '../components/MeditationList.vue';
import UserProfile from '../components/UserProfile.vue';
</script>

<template>
  <main class="main">
    <UserProfile />
    <MeditationList />
  </main>
</template>

<style scope>
.main {
  display: flex;
  justify-content: space-between;
  gap: 50px;
}
</style>
