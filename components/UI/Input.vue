<script setup lang="ts">
defineProps({
  value: {
    type: String,
    required: true,
  },
  label: {
    type: String,
    default: null,
  }
})
</script>

<template>
  <div>
    <label for="" v-if="label" class="block pl-3 ml-px text-sm font-medium text-gray-700">{{ label }}</label>
    <input :value="value" :label="label"
           class="block px-4 w-full border-gray-300 rounded-full shadow-sm focus:ring-blue-500 focus:border-blue-500 sm:text-sm"/>
  </div>
</template>

