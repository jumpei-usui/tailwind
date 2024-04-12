<script setup lang="ts">
withDefaults(
  defineProps<{
    color?: "red" | "blue" | "green" | "yellow" | "black" | "special";
  }>(),
  {
    color: "blue",
  },
);

const colorVariants = {
  red: "btn-red",
  blue: "btn-blue",
  green: "btn-green",
  yellow: "btn-yellow",
  black: "btn-black",
  special: "btn-special",
};
</script>

<template>
  <button :class="[colorVariants[color], 'btn-shape']">
    <slot />
  </button>
</template>
