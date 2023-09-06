<template>
  <header class="flex p-2 justify-between items-center">
    <div class="flex space-x-2 items-center">
      <StoryBox
        size="sm"
        :avatar="avatar"
        :seen="storySeen"
        :username="username"
        :put-username="false"
      />
      <span class="text-base font-bold hover:underline cursor-pointer">{{
        username
      }}</span>
    </div>
    <ThreeSmallDot />
  </header>
</template>
<script setup lang="ts">
import StoryBox from "../Story/Box.vue";
import ThreeSmallDot from "../Icons/ThreeSmallDot.vue";
defineProps<{
  username: string;
  image: string;
  avatar: string;
  description?: string;
  storySeen?: boolean;
}>();
</script>
