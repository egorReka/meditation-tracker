<script setup lang="ts">
import MainHeader from '@/components/MainHeader.vue';


</script>

<template>
  <div class="wrapper">
    <MainHeader />

    <RouterView />
  </div>
</template>

<style scope>
.wrapper {
  display: grid;
  grid-template-rows: auto 1fr;
  row-gap: 48px;
  padding: 40px 60px;
  min-height: 100svh;
}
</style>
