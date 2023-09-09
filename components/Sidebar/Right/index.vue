<template>
  <div class="flex flex-col">
    <SidebarRightPreviewCard title="Whats Happening">
      <SidebarRightPreviewCardItem
        v-for="(item, index) in whatsHappeningItems"
        :key="index"
      >
        <div>
          <h2 class="font-semibold text-gray-800 text-md dark:text-white">
            {{ item.title }}
          </h2>
          <p class="text-xs text-gray-500 dark:text-white">{{ item.count }}</p>
        </div>
      </SidebarRightPreviewCardItem>
    </SidebarRightPreviewCard>

    <SidebarRightPreviewCard title="Who to Follow">
      <SidebarRightPreviewCardItem
        v-for="(item, index) in whoToFollowItems"
        :key="index"
      >
        <div class="flex flex-row items-center justify-between p-2 cursor-default">
          <div class="flex flex-row items-center gap-3">
            <img :src="item.image" alt="" class="w-10 h-10 rounded-full" />
            <div>
              <h2 class="font-semibold text-gray-800 text-md dark:text-white">
                {{ item.name }}
              </h2>
              <p class="text-sm text-gray-500 dark:text-white">{{ item.handle }}</p>
            </div>
          </div>
          <div class="flex items-center h-full">
            <button class="text-sm font-semibold text-dark dark:text-white">Follow</button>
          </div>
        </div>
      </SidebarRightPreviewCardItem>
    </SidebarRightPreviewCard>
  </div>
</template>

<script setup>
const whatsHappeningItems = ref([
  {
    title: "SpaceX",
    count: "12.6k views",
  },
  {
    title: "SpaceX",
    count: "12.6k views",
  },
  {
    title: "SpaceX",
    count: "12.6k views",
  },
]);
const whoToFollowItems = ref([
  {
    name: "Munns",
    handle: "@username",
    image: "https://picsum.photos/200/200",
  },
  {
    name: "Ahmed",
    handle: "@username",
    image: "https://picsum.photos/200/200",
  },
  {
    name: "Pintu",
    handle: "@username",
    image: "https://picsum.photos/200/200",
  },
]);
</script>