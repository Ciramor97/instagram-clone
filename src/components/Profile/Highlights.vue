<template>
  <section
    class="px-4 py-2 no-scrollbar space-x-4 flex overflow-x-auto flex-shrink-1"
  >
    <StoryBox
      v-for="item in 8"
      :avatar="`https://picsum.photos/id/${item + 300}/200/200`"
      seen
      contrast
      :username="`${emojis[item]}`"
    />
  </section>
</template>

<script setup lang="ts">
import StoryBox from "../Story/Box.vue";

const emojis = [
  "✨ Paris",
  "🔥 Marseille",
  "🎉 Montpellier",
  "🤯 Rennes",
  "💅 Dijon",
  "🙇‍♂️ Barcelone",
  "😍 Lyon",
  "🥶 Lille",
];
</script>
