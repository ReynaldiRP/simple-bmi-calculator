<template>
  <div
    class="flex flex-col justify-center items-center gap-3 w-[390px] h-[225px] shadow-[0_3px_10px_rgb(0,0,0,0.2)] rounded-xl"
  >
    <h3 class="text-xl font-extrabold text-green-500">Height (CM)</h3>
    <div
      class="flex justify-around items-center w-[90%] h-3/5 bg-green-500 rounded-xl text-slate-600"
    >
      <button @click="incrementHeight">
        <i class="fa-solid fa-arrow-up text-3xl"></i>
      </button>
      <input
        type="number"
        :value="height"
        @input="updateHeight"
        class="w-1/2 text-5xl font-extrabold rounded-xl bg-transparent text-center"
      />
      <button @click="decrementHeight">
        <i class="fa-solid fa-arrow-down text-3xl"></i>
      </button>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from 'vue'

defineProps({
  height: Number,
  incrementHeight: Function,
  decrementHeight: Function,
  updateHeight: Function
})
</script>
