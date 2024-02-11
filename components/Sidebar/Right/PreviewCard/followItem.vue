<script setup>

const props = defineProps({
  name: {
    type: String,
    required: true,
  },
  handle: {
    type: String,
    required: true,
  },
  image: {
    type: String,
    default: 'https://picsum.photos/200/200'
  }
})

const {twitterBorderColor, defaultTransition} = useTailwindConfig()
const wrapperClasses = computed(() => `${twitterBorderColor} ${defaultTransition}`)
</script>

<template>
  <div class="p-3 hover:bg-gray-100 cursor-pointer hover:dark:bg-dim-300 border-b" :class=wrapperClasses>
    <div class="flex flex-row justify-between items-center p-2">
      <div class="flex flex-row">
        <img :src="props.image" class="w-10 h-10 rounded-full" :alt="props.name"/>
        <div class="flex flex-col ml-2">
          <h1 class="text-sm font-bold text-gray-900 dark:text-white">{{ props.name }}</h1>
          <p class="text-xs text-gray-400">{{ props.handle }}</p>
        </div>
      </div>
      <button class="px-4 py-2 font-bold text-xs text-white dark:text-black bg-black dark:bg-white rounded-full">
        Follow
      </button>
    </div>
  </div>

</template>