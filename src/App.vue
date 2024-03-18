<template>
  <div class="min-h-screen flex flex-col gap-6 items-center justify-center">
    <HeaderApp />
    <div class="container flex justify-center gap-6">
      <PersonAge :age="age" :incrementAge="incrementAge" :decrementAge="decrementAge" />
      <PersonWeight
        :weight="weight"
        :incrementWeight="incrementWeight"
        :decrementWeight="decrementWeight"
      />
    </div>
  </div>
</template>

<script setup>
import HeaderApp from '@/components/HeaderApp.vue'
import PersonAge from '@/components/PersonAge.vue'
import PersonWeight from '@/components/PersonWeight.vue'
import { ref } from 'vue'

const age = ref(0)
const weight = ref(0)

// Increment the Age
const incrementAge = () => {
  return age.value++
}
// Decrement the Age
const decrementAge = (e) => {
  if (age.value <= 0) {
    return e.preventDefault()
  }
  return age.value--
}

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
</script>
