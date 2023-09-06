<template>
  <header class="p-4 flex justify-between items-center border-b">
    <div class="flex space-x-2 items-center">
      <h1 class="font-semibold text-xl">{{ name }}</h1>
      <IconChevronDown class="text-sm inline" />
    </div>
    <div class="flex space-x-3 items-center text-2xl">
      <PlusIcon />
      <MenuIcon />
    </div>
  </header>
</template>
<script setup lang="ts">
import IconChevronDown from "~icons/tabler/chevron-down";
import PlusIcon from "~icons/tabler/square-plus";
import MenuIcon from "~icons/tabler/menu-2";
defineProps<{
  name: string;
}>();
</script>
