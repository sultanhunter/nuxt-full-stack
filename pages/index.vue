<script setup>
const loading = ref(false)

definePageMeta({
  middleware: 'auth',
  layout: 'authenticated'
})

</script>

<template>
  <div>
    <MainSection title="Home" :loading="loading">
      Content
    </MainSection>
  </div>
</template>