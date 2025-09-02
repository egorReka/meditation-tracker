<script setup lang="ts"></script>

<template>
  <button class="button-feel">
    <div class="button-feel__icon">
      <slot name="icon"></slot>
    </div>

    <span class="button-feel__text">
      <slot></slot>
    </span>
  </button>
</template>

<style scope>
.button-feel {
  display: grid;
  row-gap: 5px;
  justify-items: center;
  padding: 0;
  font-weight: 400;
  font-size: 12px;
  text-transform: capitalize;
  color: var(--color-default-white);
  background-color: transparent;
  border: none;
  cursor: pointer;
}

.button-feel:hover .button-feel__icon {
  background-color: var(--color-keppel);
}

.button-feel__icon {
  display: grid;
  place-content: center;
  width: 62px;
  height: 65px;
  border-radius: 20px;
  background-color: var(--color-default-white);
  opacity: 0.9;
  transition: background-color 0.2s;
}
</style>
