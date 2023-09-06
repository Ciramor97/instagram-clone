<template>
  <div class="flex flex-col space-y-3">
    <h4 class="font-medium text-sm">{{ title }}</h4>
    <slot></slot>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  title: string;
}>();
</script>
