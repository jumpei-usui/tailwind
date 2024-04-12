<script setup lang="ts">
const open = defineModel<boolean>({ default: false });
</script>

<template>
  <div
    class="absolute h-screen w-32 bg-black transition-all"
    :class="open ? 'left-0' : '-left-32'"
  >
    <div class="cursor-pointer p-4 text-white" @click="open = false">close</div>
    <div class="cursor-pointer p-4 text-white">aaa</div>
    <div class="cursor-pointer p-4 text-white">aaa</div>
    <div class="absolute bottom-0 cursor-pointer p-4 text-white">setting</div>
  </div>
</template>
