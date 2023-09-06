<template>
  <div class="w-full">
    <Header
      :username="username"
      :image="image"
      :avatar="avatar"
      :description="description"
      :story-seen="storySeen"
    ></Header>
    <ImageContent :image="image"></ImageContent>
    <Footer
      :username="username"
      :image="image"
      :avatar="avatar"
      :description="description"
      :story-seen="storySeen"
    ></Footer>
  </div>
</template>

<script setup lang="ts">
import Header from "./Header.vue";
import Footer from "./Footer.vue";
import ImageContent from "./Image.vue";
defineProps<{
  username: string;
  image: string;
  avatar: string;
  description?: string;
  storySeen?: boolean;
}>();
</script>
