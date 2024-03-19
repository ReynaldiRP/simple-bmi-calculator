<template>
  <div class="min-h-screen py-6 flex flex-col gap-6 items-center justify-center">
    <HeaderApp />
    <div class="container flex flex-col items-center gap-6">
      <div class="flex justify-center gap-6">
        <PersonAge />
        <PersonWeight />
      </div>
      <PersonHeight />
      <PersonGender />
    </div>
  </div>
</template>

<script setup>
import HeaderApp from '@/components/HeaderApp.vue'
import PersonAge from '@/components/PersonAge.vue'
import PersonHeight from '@/components/PersonHeight.vue'
import PersonWeight from '@/components/PersonWeight.vue'
import PersonGender from '@/components/PersonGender.vue'
</script>
