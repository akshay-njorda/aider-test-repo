<template>
  <div class="space-y-4">
    <h2 class="text-xl font-semibold">Personal Information</h2>
    <div class="space-y-4">
      <div>
        <label class="block text-sm font-medium text-gray-700">Full Name</label>
        <input
          v-model="formStore.formData.name"
          type="text"
          class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500"
          placeholder="Enter your full name"
        />
      </div>
      <div>
        <label class="block text-sm font-medium text-gray-700">Email</label>
        <input
          v-model="formStore.formData.email"
          type="email"
          class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500"
          placeholder="Enter your email"
        />
      </div>
    </div>
  </div>
</template>

<script setup>
import { useFormStore } from '~/stores/form'

const formStore = useFormStore()
</script>
