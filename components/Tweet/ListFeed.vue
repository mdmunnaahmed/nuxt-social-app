<template>
  <div>
    <ul>
      <TweetItem
        v-for="(tweet, index) in props.tweets"
        :key="index"
        :name="tweet.name"
        :title="tweet.title"
        :user="tweet.image"
        :image="tweet.image"
        :handler="tweet.handler"
        :totalComments="tweet.totalComments"
        :totalLove="tweet.totalLove"
        :totalRePosts="tweet.totalRePosts"
      ></TweetItem>
    </ul>
  </div>
</template>

<script setup>
const props = defineProps({
  tweets: {
    type: Array,
    required: false,
  },
});
</script>