<script setup lang="ts">
import { useRouter } from 'vue-router';

const router = useRouter();

function redirectToMain() {
  router.push(
    { name: 'main' }
  );
}
</script>

<template>
  <button class="button-auth" type="button" @click="redirectToMain">
    <slot></slot>
  </button>

</template>

<style scope>
.button-auth {
  display: block;
  width: 100%;
  padding: 15px 40px;
  font-weight: 500;
  font-size: 25px;
  border: none;
  border-radius: 10px;
  background-color: var(--color-granny-smith);
  color: var(--color-default-white);
  cursor: pointer;
  transition: opacity 0.2s;
}

.button-auth:hover,
.button-auth:focus {
  opacity: 0.7;
}
</style>
