<script setup lang="ts">
const val = ref("");
const open = ref(false);

const func = () => {
  const x = 1;
  console.log("func");
};
</script>

<template>
  <MySlide v-model="open"></MySlide>
  <MyButton color="green">LINE</MyButton>
  <MyButton color="black" @click="open = !open">X</MyButton>
  <MyButton @click="func">Twitter</MyButton>
  <MyButton color="special">Instagram</MyButton>
  <input
    v-model="val"
    type="text"
    pattern="[a-zA-Z1-9.]+@[a-zA-Z1-9.]+"
    class="w-40 rounded-full border border-green-400 px-3 py-1 caret-green-400 invalid:border-red-600 invalid:text-red-600 invalid:caret-red-600 focus:border-2 focus:outline-none"
  />
  {{ val }}
</template>
