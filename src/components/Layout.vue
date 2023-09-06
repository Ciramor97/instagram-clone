<template>
  <div
    class="bg-white w-full min-h-screen text-black"
    :class="{ 'pt-12 pb-16': route.path == '/' }"
  >
    <slot></slot>
  </div>
</template>
<script setup lang="ts">
import { useRoute } from "vue-router";

const route = useRoute();
</script>
