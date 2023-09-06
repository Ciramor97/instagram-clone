<script lang="ts" setup>
import CameraIcon from "~icons/tabler/camera";

// Components
import StoryBox from "../Story/Box.vue";

const props = defineProps<{
  avatar?: string;
  username?: string;
}>();

const mockMessages = [
  "How are you?",
  "Seen 3 h ago",
  `${props.username} shared a reel`,
  "Active now",
  "Please 🙏",
];

const getRandomBooleanValue = Math.random() > 0.25;
const getAnotherRandomBooleanValue = Math.random() > 0.5;
const getRandomMessage =
  mockMessages[Math.floor(Math.random() * mockMessages.length)];
</script>

<template>
  <div class="flex justify-between items-center">
    <div class="flex items-center space-x-2 flex-grow">
      <StoryBox
        size="md"
        :avatar="avatar"
        :seen="getAnotherRandomBooleanValue"
      />

      <div
        class="font-light leading-snug text-sm flex-col flex"
        :class="{
          'text-black': !getRandomBooleanValue,
          'text-black/50': getRandomBooleanValue,
        }"
      >
        <span class="font-medium">{{ username }}</span>
        <span
          class="text-[0.95em]"
          :class="{
            'text-black/50': getRandomBooleanValue,
            'text-black': !getRandomBooleanValue,
          }"
          >{{ getRandomMessage }}</span
        >
      </div>
    </div>

    <div class="flex space-x-4 items-center text-[21.6px] text-black/50">
      <span
        v-if="getRandomBooleanValue"
        class="w-2 h-2 rounded-full bg-blue-600"
      ></span>
      <CameraIcon class="cursor-pointer" />
    </div>
  </div>
</template>

<style scoped>
:deep(strong) {
  @apply font-medium;
}
</style>
