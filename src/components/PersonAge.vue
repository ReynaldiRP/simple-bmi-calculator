<template>
  <div
    class="flex flex-col items-center justify-center gap-8 w-[185px] h-[225px] shadow-[0_3px_10px_rgb(0,0,0,0.2)] rounded-xl"
  >
    <h3 class="text-xl font-extrabold text-green-500">Age</h3>
    <input
      type="number"
      :value="age"
      @input="updateAge"
      class="w-1/2 text-5xl font-extrabold rounded-xl bg-transparent text-center text-slate-500"
    />
    <div class="flex gap-8">
      <button
        @click="decrementAge"
        class="w-[35px] h-[35px] bg-green-500 text-white font-bold rounded-full"
      >
        <i class="fa-solid fa-minus"></i>
      </button>
      <button
        @click="incrementAge"
        class="w-[35px] h-[35px] bg-green-500 text-white font-bold rounded-full"
      >
        <i class="fa-solid fa-plus"></i>
      </button>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from 'vue'

defineProps({
  age: Number,
  incrementAge: Function,
  decrementAge: Function,
  updateAge: Function
})
</script>
