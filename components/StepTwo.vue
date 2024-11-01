<template>
  <div class="space-y-4">
    <h2 class="text-xl font-semibold">Contact Details</h2>
    <div class="space-y-4">
      <div>
        <label class="block text-sm font-medium text-gray-700">Phone Number</label>
        <input
          v-model="formStore.formData.phone"
          type="tel"
          class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500"
          placeholder="Enter your phone number"
        />
      </div>
      <div>
        <label class="block text-sm font-medium text-gray-700">Address</label>
        <textarea
          v-model="formStore.formData.address"
          class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500"
          rows="3"
          placeholder="Enter your address"
        ></textarea>
      </div>
    </div>
  </div>
</template>

<script setup>
import { useFormStore } from '~/stores/form'

const formStore = useFormStore()
</script>
