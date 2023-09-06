<template>
  <section class="grid grid-cols-3">
    <div
      v-for="(item, index) in items"
      class="border-b border-black/10 py-2 select-none cursor-pointer text-sm hover:border-black/50 transition-colors text-center"
      :class="{
        'border-black text-black': activeItemIndex === index,
        'text-black/50': activeItemIndex !== index,
      }"
      @click="chooseItem(index)"
    >
      <component
        v-if="isComponentItem"
        :is="item"
        class="text-2xl mx-auto"
      ></component
      ><span v-else class="mx-auto">{{ item }}</span>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from "vue";

const activeItemIndex = ref(0);

withDefaults(
  defineProps<{
    items: any[];
    isComponentItem: boolean;
  }>(),
  {
    isComponentItem: true,
  }
);

function chooseItem(itemIndex: number) {
  activeItemIndex.value = itemIndex;
}
</script>
