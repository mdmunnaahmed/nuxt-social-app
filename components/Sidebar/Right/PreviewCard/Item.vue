<template>
  <div
    class="p-3 hover:bg-gray-100 cursor-pointer dark:hover:bg-dim-300 border-b"
    :class="wrapperClass"
  >
    <slot />
  </div>
</template>

<script setup>
const { defaultTransition, twitterBorderColor } = useTailwindConfig();
const wrapperClass = computed(
  () => `${defaultTransition} + ${twitterBorderColor}`
);
</script>