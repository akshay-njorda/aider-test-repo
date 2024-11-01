<template>
  <div class="w-full py-6">
    <div class="flex items-center">
      <div v-for="step in 4" :key="step" class="flex items-center">
        <div
          :class="[
            'flex h-12 w-12 items-center justify-center rounded-full border-2 font-semibold',
            formStore.currentStep >= step
              ? 'border-indigo-600 bg-indigo-600 text-white'
              : 'border-gray-300 text-gray-500'
          ]"
        >
          {{ step }}
        </div>
        <div
          v-if="step < 4"
          :class="[
            'h-0.5 w-full',
            formStore.currentStep > step ? 'bg-indigo-600' : 'bg-gray-300'
          ]"
        ></div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { useFormStore } from '~/stores/form'

const formStore = useFormStore()
</script>
