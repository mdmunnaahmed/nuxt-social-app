<template>
  <div>
    <MainSection title="Home" :loading="loading">
      <TweetListFeed :tweets="tweets" />
    </MainSection>
  </div>
</template>

<script setup>
const loading = ref(false);
const tweets = ref([
  {
    title: "this is a demo tweet",
    name: "Munns",
    handler: "username",
    image: "https://picsum.photos/550/550",
    totalComments: "14.8k",
    totalRePosts: "5.9k",
    totalLove: "92",
  },
  {
    title: "this is a demo tweet",
    name: "Munns",
    handler: "username",
    image: "https://picsum.photos/550/550",
    totalComments: "14.8k",
    totalRePosts: "5.9k",
    totalLove: "92",
  },
  {
    title: "this is a demo tweet",
    name: "Munns",
    handler: "username",
    image: "https://picsum.photos/550/550",
    totalComments: "14.8k",
    totalRePosts: "5.9k",
    totalLove: "92",
  },
]);
</script>
