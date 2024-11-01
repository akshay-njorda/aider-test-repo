<template>
  <div class="space-y-4">
    <h2 class="text-xl font-semibold">Review & Submit</h2>
    <div class="space-y-4 bg-gray-50 p-4 rounded-lg">
      <div v-if="formStore.formData.name" class="flex justify-between">
        <span class="font-medium">Name:</span>
        <span>{{ formStore.formData.name }}</span>
      </div>
      <div v-if="formStore.formData.email" class="flex justify-between">
        <span class="font-medium">Email:</span>
        <span>{{ formStore.formData.email }}</span>
      </div>
      <div v-if="formStore.formData.phone" class="flex justify-between">
        <span class="font-medium">Phone:</span>
        <span>{{ formStore.formData.phone }}</span>
      </div>
      <div v-if="formStore.formData.address" class="flex justify-between">
        <span class="font-medium">Address:</span>
        <span>{{ formStore.formData.address }}</span>
      </div>
      <div v-if="formStore.formData.contactPreference" class="flex justify-between">
        <span class="font-medium">Contact Preference:</span>
        <span>{{ formStore.formData.contactPreference }}</span>
      </div>
      <div class="flex justify-between">
        <span class="font-medium">Newsletter:</span>
        <span>{{ formStore.formData.newsletter ? 'Yes' : 'No' }}</span>
      </div>
    </div>
  </div>
</template>

<script setup>
import { useFormStore } from '~/stores/form'

const formStore = useFormStore()
</script>
