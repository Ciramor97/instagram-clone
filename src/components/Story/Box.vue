<template>
  <div class="flex flex-shrink-0 flex-col items-center cursor-pointer">
    <div
      class="rounded-full p-0.5"
      :class="{
        'from-purple-600  via-red-600 to-yellow-500 bg-gradient-to-bl':
          !seen && showCircle,
        'bg-gray-200': seen && showCircle,
      }"
      @click="handleStoryBoxClick"
    >
      <img
        v-if="avatar !== ''"
        :src="`https://proxy.duckduckgo.com/iu/?u=${avatar}`"
        alt="cool"
        class="object-cover rounded-full"
        :class="{
          'w-[100px] h-[100px]': size === 'lg',
          'w-[65px] h-[65px]': size === 'normal',
          'w-[55px] h-[55px]': size === 'md',
          'w-[40px] h-[40px]': size === 'sm',
          'w-[30px] h-[30px]': size === 'xs',
          'border-2 border-white': seen,
        }"
        loading="lazy"
        draggable="false"
      />
      <img
        v-else
        src="../../assets/roma-dev.jpg"
        alt="Roma dev"
        class="object-cover rounded-full"
        :class="{
          'w-[100px] h-[100px]': size === 'lg',
          'w-[65px] h-[65px]': size === 'normal',
          'w-[55px] h-[55px]': size === 'md',
          'w-[40px] h-[40px]': size === 'sm',
          'w-[30px] h-[30px]': size === 'xs',
          'border-2 border-white': seen,
        }"
        loading="lazy"
        draggable="false"
      />
    </div>
    <span
      v-if="putUsername && username"
      class="text-sm"
      :class="{
        'text-black text-xs': contrast,
        'text-black/50': !contrast && seen,
        'text-black/75': !contrast && !seen,
      }"
    >
      {{ username }}
    </span>
  </div>
</template>

<script setup lang="ts">
import useDataStore from "../../store/data";

const props = withDefaults(
  defineProps<{
    avatar?: string;
    seen?: boolean;
    username?: string;
    size?: "normal" | "sm" | "xs" | "md" | "lg";
    showCircle?: boolean;
    putUsername?: boolean;
    contrast?: boolean;
  }>(),
  {
    size: "normal",
    showCircle: true,
    putUsername: true,
  }
);

const store = useDataStore();

function handleStoryBoxClick() {
  if (!props.username) return;
  store.toggleStorySeen(props.username);
}
</script>
