<script setup>

const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  count: {
    type: String,
    required: true,
  }
})

const {twitterBorderColor, defaultTransition} = useTailwindConfig()
const wrapperClasses = computed(() => `${twitterBorderColor} ${defaultTransition}`)
</script>

<template>
  <div class="p-3 hover:bg-gray-100 cursor-pointer hover:dark:bg-dim-300 border-b" :class=wrapperClasses>
    <div>
      <h2 class="font-bold text-gray-800 text-md dark:text-white">{{ props.title }}</h2>
      <p class="text-xs text-gray-400">{{ props.count }}</p>
    </div>
  </div>
</template>