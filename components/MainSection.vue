<template>
  <div>
    <div class="sticky top-0 bg-white/80 backdrop-blur-md dark:bg-dim-900/80">
      <h2 class="font-semibold text-md text-gray-800 dark:text-gray-100">
        {{ props.title }}
      </h2>
    </div>
    <div v-if="loading" class="flex items-center justify-center border-b py-3">
      <UISpinner />
    </div>
    <div v-else><slot /></div>
  </div>
</template>

<script setup>
const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  loading: {
    type: Boolean,
    required: true,
  },
});
</script>
