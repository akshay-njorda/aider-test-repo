<template>
  <div class="space-y-4">
    <h2 class="text-xl font-semibold">Preferences</h2>
    <div class="space-y-4">
      <div>
        <label class="block text-sm font-medium text-gray-700">Preferred Contact Method</label>
        <select
          v-model="formStore.formData.contactPreference"
          class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500"
        >
          <option value="email">Email</option>
          <option value="phone">Phone</option>
          <option value="mail">Mail</option>
        </select>
      </div>
      <div>
        <label class="block text-sm font-medium text-gray-700">Newsletter Subscription</label>
        <div class="mt-2">
          <label class="inline-flex items-center">
            <input
              v-model="formStore.formData.newsletter"
              type="checkbox"
              class="rounded border-gray-300 text-indigo-600 shadow-sm focus:border-indigo-500 focus:ring-indigo-500"
            />
            <span class="ml-2">Subscribe to our newsletter</span>
          </label>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { useFormStore } from '~/stores/form'

const formStore = useFormStore()
</script>
