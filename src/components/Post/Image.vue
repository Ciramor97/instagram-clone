<template>
  <img
    v-if="image === ''"
    src="../../assets/roma-dev.jpg"
    alt="Roma dev"
    class="w-full object-cover aspect-square"
  />
  <img
    v-else
    :src="image"
    alt="Posted image"
    class="w-full object-cover aspect-square"
  />
</template>
<script setup lang="ts">
defineProps<{
  image: string;
}>();
</script>
