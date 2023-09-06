<template>
  <StoryContainer>
    <StoryBox
      v-for="(data, index) in store.data"
      :key="index"
      :avatar="data.image"
      :seen="data.storySeen"
      :username="data.user.nickname"
    />
  </StoryContainer>

  <PostContainer>
    <PostBox
      v-for="(post, index) in store.getRandomizedData"
      :key="`post-${index}`"
      :username="post.user.nickname"
      :avatar="post.user.avatar"
      :image="post.image"
      :description="post.description"
      :story-seen="post.storySeen"
    />
  </PostContainer>
</template>
<script setup lang="ts">
import StoryContainer from "../components/Story/Container.vue";
import StoryBox from "../components/Story/Box.vue";

import PostContainer from "../components/Post/Container.vue";
import PostBox from "../components/Post/Box.vue";

import useDataStore from "../store/data";

const store = useDataStore();
</script>
