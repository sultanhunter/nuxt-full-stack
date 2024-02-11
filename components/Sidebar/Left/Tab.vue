<script setup>
const {defaultTransition} = useTailwindConfig()

const props = defineProps({
  active: {
    type: Boolean,
    default: false,
  }
})

const textClasses = computed(() => props.active ? "font-semibold" : "font-norma")
</script>


<template>
  <NuxtLink to="#" class="flex items-center rounded-full p-3  hover:bg-gray-200
   text-black dark:hover:bg-dim-200 dark:text-white">
    <div class="h-6 w-6 text-dark" :class=defaultTransition>
      <slot name="icon"/>
    </div>

    <div class="hidden xl:block ml-4 text-xl" :class="textClasses">
      <slot name="name"/>
    </div>
  </NuxtLink>
</template>