<template>
  <div class="w-full px-4 relative">
    <SearchIcon class="absolute inset-y-0 left-6 h-full text-black/30" />
    <input
      :id="name"
      :type="type"
      :placeholder="placeholder"
      class="w-full rounded-lg bg-black/10 px-8 py-1 outline-none appearance-none placeholder:text-black/30 text-black"
      :value="modelValue"
      @input="updateInput"
    />
  </div>
</template>
<script setup lang="ts">
import SearchIcon from "~icons/tabler/search";

interface Props {
  placeholder?: string;
  name?: string;
  type: string;
  modelValue: string | number;
}

withDefaults(defineProps<Props>(), {
  placeholder: "Search",
  type: "text",
  modelValue: "",
});

const emit = defineEmits<{
  (e: "update:modelValue", value: string | number): void;
}>();

function updateInput(event: Event) {
  emit("update:modelValue", (event.target as any).value);
}
</script>
