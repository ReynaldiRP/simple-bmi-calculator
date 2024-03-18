<template>
  <div class="min-h-screen flex flex-col gap-6 items-center justify-center">
    <HeaderApp />
    <div class="container flex flex-col items-center gap-6">
      <div class="flex justify-center gap-6">
        <PersonAge
          :age="age"
          :incrementAge="incrementAge"
          :decrementAge="decrementAge"
          :updateAge="updateAge"
        />
        <PersonWeight
          :weight="weight"
          :incrementWeight="incrementWeight"
          :decrementWeight="decrementWeight"
          :updateWeight="updateWeight"
        />
      </div>
      <PersonHeight
        :height="height"
        :incrementHeight="incrementHeight"
        :decrementHeight="decrementHeight"
        :updateHeight="updateHeight"
      />
    </div>
  </div>
</template>

<script setup>
import HeaderApp from '@/components/HeaderApp.vue'
import PersonAge from '@/components/PersonAge.vue'
import PersonWeight from '@/components/PersonWeight.vue'
import PersonHeight from '@/components/PersonHeight.vue'
import { ref } from 'vue'

const age = ref(0)
const weight = ref(0)
const height = ref(0)

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
// Update Age Value
const updateAge = (e) => {
  return (age.value = Number(e.target.value))
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
// Update Weight Value
const updateWeight = (e) => {
  return (weight.value = Number(e.target.value))
}

// Increment the Height
const incrementHeight = () => {
  return height.value++
}
// Decrement the Height
const decrementHeight = (e) => {
  if (height.value <= 0) {
    return e.preventDefault()
  }
  return height.value--
}
// Update Height Value
const updateHeight = (e) => {
  return (height.value = Number(e.target.value))
}
</script>
