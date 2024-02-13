<script setup>
const darkMode = ref(false)

</script>


<template>
  <div :class="{'dark':darkMode}">
    <div class="min-h-full bg-white dark:bg-dim-900">

      <!-- Authenticated App -->
      <div class="grid grid-cols-12 mx-auto sm:px-6 lg:max-w-7xl lg:px-8 md:gap-5">

        <!--Left Sidebar-->
        <div class="hidden border-2 border-red-300 md:block md:col-span-1 xl:col-span-2 ">
          <div class="sticky top-0">
            <SidebarLeft/>
          </div>
        </div>

        <!--Main Content -->
        <main class="col-span-12 md:col-span-8 xl:col-span-6">
          <slot/>
        </main>

        <!--Right Sidebar -->
        <div class="hidden border-2 border-red-300 md:block md:col-span-3 xl:col-span-4 ">
          <div class="sticky top-0">
            <SidebarRight/>
          </div>
        </div>


      </div>


    </div>
  </div>
</template>