<template>
  <div class="grid grid-cols-1 gap-6 place-items-center">
    <div
      class="flex flex-col justify-center items-center gap-3 w-[390px] h-[225px] shadow-[0_3px_10px_rgb(0,0,0,0.2)] rounded-xl cursor-pointer border-none"
    >
      <h3 class="text-xl font-extrabold text-green-500">Genders</h3>
      <div class="grid grid-cols-2 gap-2 p-4">
        <label>
          <input type="radio" @click="toggleActive('male')" class="peer hidden" name="framework" />

          <div
            class="hover:bg-gray-50 flex items-center justify-between px-4 py-2 border-2 rounded-lg cursor-pointer text-sm border-gray-200 group peer-checked:border-green-500"
          >
            <h2 class="font-medium text-gray-700">Male</h2>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              class="w-9 h-9 text-green-600 invisible group-[.peer:checked+&]:visible"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M9 12.75L11.25 15 15 9.75M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
              />
            </svg>
          </div>
        </label>
        <label>
          <input
            type="radio"
            @click="toggleActive('female')"
            class="peer hidden"
            name="framework"
          />

          <div
            class="hover:bg-gray-50 flex items-center justify-between px-4 py-2 border-2 rounded-lg cursor-pointer text-sm border-gray-200 group peer-checked:border-green-500"
          >
            <h2 class="font-medium text-gray-700">Female</h2>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              class="w-9 h-9 text-green-600 invisible group-[.peer:checked+&]:visible"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M9 12.75L11.25 15 15 9.75M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
              />
            </svg>
          </div>
        </label>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const isActive = ref([])

const toggleActive = (value) => {
  isActive.value = isActive.value.includes(value)
    ? isActive.value.filter((item) => item != value)
    : [...isActive.value, value]

  console.log(value)
}
</script>
