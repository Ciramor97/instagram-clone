<template>
  <nav class="py-4 flex justify-between items-center">
    <div
      class="flex space-x-2 items-center cursor-pointer"
      @click="router.back()"
    >
      <IconChevronLeft class="text-2xl inline" />
      <h1 class="font-semibold text-lg">Roma_dev</h1>
      <IconChevronDown class="text-xs inline" />
    </div>
    <div class="flex space-x-4 items-center text-2xl">
      <ListIcon />
      <DocumentIcon />
    </div>
  </nav>
</template>
<script setup lang="ts">
import IconChevronDown from "~icons/tabler/chevron-down";
import IconChevronLeft from "~icons/tabler/chevron-left";
import ListIcon from "~icons/tabler/list";
import DocumentIcon from "~icons/tabler/file-pencil";
import { useRouter } from "vue-router";

const router = useRouter();
</script>
