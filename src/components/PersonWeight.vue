<template>
  <div
    class="flex flex-col items-center justify-center gap-8 w-[185px] h-[225px] shadow-[0_3px_10px_rgb(0,0,0,0.2)] rounded-xl"
  >
    <h3 class="text-xl font-extrabold text-green-500">Weight (KG)</h3>
    <input
      type="number"
      :value="weight"
      @input="updateWeight"
      class="w-1/2 text-5xl font-extrabold rounded-xl bg-transparent text-center text-slate-500"
    />
    <div class="flex gap-8">
      <button
        @click="decrementWeight"
        class="w-[35px] h-[35px] bg-green-500 text-white font-bold rounded-full"
      >
        <i class="fa-solid fa-minus"></i>
      </button>
      <button
        @click="incrementWeight"
        class="w-[35px] h-[35px] bg-green-500 text-white font-bold rounded-full"
      >
        <i class="fa-solid fa-plus"></i>
      </button>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const weight = ref(0)

// Increment the Weight
const incrementWeight = () => {
  return weight.value++
}
// Decrement the Weight
const decrementWeight = (e) => {
  if (weight.value <= 0) {
    return e.preventDefault()
  }
  return weight.value--
}
// Update Weight Value
const updateWeight = (e) => {
  return (weight.value = Number(e.target.value))
}
</script>
