<template>
  <footer class="flex flex-col px-4 py-2">
    <div class="flex items-center justify-between">
      <div class="flex space-x-3 [&>*]:cursor-pointer items-center">
        <IconHeart :animation="true" />
        <IconChat class="h-8 w-8" />
        <IconPaperAirplane />
      </div>
      <button @click="bookmarked = !bookmarked">
        <IconBookmark
          class="cursor-pointer"
          :class="{ 'text-yellow-300': bookmarked }"
        />
      </button>
    </div>
    <span class="mb-1 font-bold mt-3 hover:underline cursor-pointer"
      >{{ getRandomNumber(100000, 10) }} J'aime</span
    >
    <div class="space-y-2">
      <p class="space-x-2 lineclamp3">
        <span class="font-bold hover:underline cursor-pointer">{{
          username
        }}</span>
        <span>{{ description }}</span>
      </p>
      <span class="text-black/50 hover:underline cursor-pointer"
        >Voir les {{ getRandomNumber(250) }} commentaires</span
      >
    </div>
    <span class="mt-1.5 font-light text-black/50 text-xs">
      Il y a
      {{ getRandomNumber(23, 0) }} jours</span
    >
  </footer>
</template>
<script setup lang="ts">
import IconChat from "~icons/tabler/message-circle";
import IconHeart from "../Icons/Heart.vue";
import IconPaperAirplane from "../Icons/PaperAirplane.vue";
import IconBookmark from "../Icons/Bookmark.vue";
import { ref } from "vue";
import { getFormattedNumberValue } from "../../functions/getFormattedNumber";

const bookmarked = ref(false);
defineProps<{
  username: string;
  description?: string;
}>();

// a function that return a number between 10 and 100000
const getRandomNumber = (maxValue: number, startValue: number = 1) =>
  getFormattedNumberValue(Math.floor(Math.random() * maxValue) + startValue);
</script>
