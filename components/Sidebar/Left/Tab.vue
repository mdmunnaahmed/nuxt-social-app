<template>
  <div>
    <nuxt-link
      to="/"
      class="flex gap-4 items-center p-3 px-5 w-min hover:bg-gray-200 rounded-full dark:hover:bg-dim-200 dark:text-white"
    >
      <div class="w-6 h-6 text-dark" :class="defaultTransition">
        <slot name="icon" />
      </div>
      <div :class="textClasses">
        <slot name="name" />
      </div>
    </nuxt-link>
  </div>
</template>

<script setup>
const { defaultTransition } = useTailwindConfig();

const props = defineProps({
  active: {
    type: Boolean,
    default: false,
  },
});
const textClasses = computed(() =>
  props.active ? "font-semibold" : "font-normal"
);
</script>