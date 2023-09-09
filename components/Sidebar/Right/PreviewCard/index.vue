<template>
  <div
    class="m-2 border bg-gray-50 rounded-2xl dark:bg-dim-700"
    :class="twitterBorderColor"
  >
    <h1 class="p-3 text-xl font-bold text-gray-900 border-b dark:text-white">
      {{ props.title }}
    </h1>
    <slot />
    <div
      class="p-3 text-sm text-blue-600 hover:bg-gray-100 dark:text-white dark:hover:bg-dim-300"
      :class="defaultTransition"
    >
      Show More
    </div>
  </div>
</template>

<script setup>
const { twitterBorderColor, defaultTransition } = useTailwindConfig();
const props = defineProps({
  title: {
    type: String,
    required: true,
  },
});
</script>