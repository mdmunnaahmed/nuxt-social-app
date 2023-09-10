<template>
  <li class="border-b py-5">
    <div class="flex items-center gap-2">
      <img :src="user" alt="image" class="w-10 h-10 rounded-full" />
      <h4 class="name">{{ name }}</h4>
      <p class="name text-gray-500 text-sm">@{{ handler }}</p>
      <small class="name">{{ postDate }}</small>
    </div>
    <p class="mb-2 mt-3 text-gray-700">{{ title }}</p>
    <img :src="image" alt="post image" class="w-full h-64 object-cover" />
    <ul class="flex gap-4 flex-row mt-4 text-gray-500 justify-between">
      <li>
        <a class="flex gap-3" href="#0"
          ><RefreshIcon class="w-6 h-6" /> {{ totalComments }}</a
        >
      </li>
      <li>
        <span class="flex gap-3 cursor-pointer" @click="toggleLove" :data-id="totalLove"
          ><HeartIcon class="w-6 h-6" />{{ totalLove }}</span
        >
      </li>
      <li>
        <a class="flex gap-3" href=""
          ><ReplyIcon class="w-6 h-6" /> {{ totalRePosts }}</a
        >
      </li>
    </ul>
  </li>
</template>


<script setup>
function toggleLove(event) {
  if (event.target.classList.contains("loved")) {
    event.target.classList.remove("loved");
  } else {
    event.target.classList.add("loved");
  }
}

import { HeartIcon, RefreshIcon, ReplyIcon } from "@heroicons/vue/outline";
const props = defineProps({
  user: String,
  name: String,
  handler: String,
  postDate: String,
  title: String,
  image: String,
  totalComments: Number,
  totalLove: Number,
  totalRePosts: Number,
});
</script>


<style scoped>
.loved svg {
  fill: #777;
  outline: #777;
}
</style>