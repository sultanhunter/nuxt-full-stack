<script setup lang="ts">
import {HomeIcon} from "@heroicons/vue/24/solid"

import {
  HashtagIcon,
  BellIcon,
  InboxIcon,
  BookmarkIcon,
  DocumentTextIcon,
  UserIcon,
  EllipsisHorizontalCircleIcon
} from "@heroicons/vue/24/outline"

const {defaultTransition} = useTailwindConfig()
</script>

<template>
  <div class="h-screen flex flex-col">
    <div class="flex justify-start items-center p-2 my-2 rounded-full hover:bg-blue-50
                dark:hover:bg-white/20" :class="defaultTransition">
      <NuxtLink to="/">
        <div class="h-8 w-8">
          <LogoTwitter/>
        </div>
      </NuxtLink>
    </div>

    <div class="mt-2 space-y-3">
      <SidebarLeftTab active>
        <template v-slot:icon>
          <HomeIcon/>
        </template>
        <template v-slot:name>
          Home
        </template>
      </SidebarLeftTab>

      <SidebarLeftTab active>
        <template v-slot:icon>
          <HashtagIcon/>
        </template>
        <template v-slot:name>
          Explore
        </template>
      </SidebarLeftTab>

      <SidebarLeftTab active>
        <template v-slot:icon>
          <BellIcon/>
        </template>
        <template v-slot:name>
          Notifications
        </template>
      </SidebarLeftTab>

      <SidebarLeftTab active>
        <template v-slot:icon>
          <InboxIcon/>
        </template>
        <template v-slot:name>
          Messages
        </template>
      </SidebarLeftTab>

      <SidebarLeftTab active>
        <template v-slot:icon>
          <BookmarkIcon/>
        </template>
        <template v-slot:name>
          Bookmarks
        </template>
      </SidebarLeftTab>

      <SidebarLeftTab active>
        <template v-slot:icon>
          <DocumentTextIcon/>
        </template>
        <template v-slot:name>
          Lists
        </template>
      </SidebarLeftTab>

      <SidebarLeftTab active>
        <template v-slot:icon>
          <UserIcon/>
        </template>
        <template v-slot:name>
          Profile
        </template>
      </SidebarLeftTab>

      <SidebarLeftTab active>
        <template v-slot:icon>
          <EllipsisHorizontalCircleIcon/>
        </template>
        <template v-slot:name>
          More
        </template>
      </SidebarLeftTab>

    </div>

  </div>
</template>

