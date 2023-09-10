<template>
  <div>
    <div class="sticky top-0 border-b bg-white backdrop-blur-md dark:bg-dim-900 px-8">
      <h2 class="font-semibold text-md text-gray-800 dark:text-gray-100 py-3">
        {{ props.title }}
      </h2>
    </div>
    <div v-if="loading" class="flex items-center justify-center border-b py-3 px-8">
      <UISpinner />
    </div>
    <div class="px-6" v-else><slot /></div>
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
