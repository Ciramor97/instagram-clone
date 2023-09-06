<template>
  <div class="px-4 py-2 gap-4 flex justify-between items-center">
    <StoryBox avatar="" size="lg" />
    <div class="flex gap-x-4 items-center text-[15px] justify-center flex-grow">
      <div class="leading-tight text-center">
        <h3 class="font-medium">26</h3>
        <span>Posts</span>
      </div>
      <div class="leading-tight text-center">
        <h3 class="font-medium">573</h3>
        <span>Followers</span>
      </div>
      <div class="leading-tight text-center">
        <h3 class="font-medium">432</h3>
        <span>Following</span>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import StoryBox from "../Story/Box.vue";
</script>
