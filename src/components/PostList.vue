<template>
  <div class="post-list"></div>
  <div v-for="post in posts" :key="post.id">
    <SinglePost :post="post" />
  </div>
</template>

<script>
import { onMounted, onUnmounted, onUpdated } from "vue";
import SinglePost from "./SinglePost.vue";

export default {
  props: ["posts"],
  components: { SinglePost },
  setup() {
    onMounted(() => console.log("mounted lol"));
    onUnmounted(() => console.log("unmounted lol"));
    onUpdated(() => console.log("updating lol"));
  },
};
</script>

<style>
</style>