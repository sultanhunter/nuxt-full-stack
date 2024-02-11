<script setup>

const whatsHappeningItems = ref([
  {title: 'SpaceX', count: '18.8k Tweets'},
  {title: '#CodingIsFun', count: '8.8k Tweets'},
  {title: '#artforall', count: '1.8k Tweets'}
],)

const whoToFollowItems = ref([
  {name: 'Joe Biden', handle: '@joeBiden', image: 'https://picsum.photos/200/200'},
  {name: 'Joe Biden', handle: '@joeBiden', image: 'https://picsum.photos/200/200'},
  {name: 'Joe Biden', handle: '@joeBiden', image: 'https://picsum.photos/200/200'},
],)

</script>

<template>
  <div class="flex flex-col ">

    <!-- Preview Card : What's Happening-->
    <SidebarRightPreviewCard title="What's Happening">
      <SidebarRightPreviewCardHappeningItem
          v-for="(whatsHappening,index) in whatsHappeningItems"
          :key="index"
          :title="whatsHappening.title"
          :count="whatsHappening.count"
      />
    </SidebarRightPreviewCard>

    <!-- Preview Card : Who to follow-->
    <SidebarRightPreviewCard title="Who to follow">
      <SidebarRightPreviewCardFollowItem
          v-for="(whoToFollow,index) in whoToFollowItems"
          :key="index"
          :name="whoToFollow.name"
          :handle="whoToFollow.handle"
          :image="whoToFollow.image"
      />
    </SidebarRightPreviewCard>

  </div>
</template>