<template>
  <header class="px-2">
    <NavBar />
    <div class="w-full px-2 relative">
      <SearchIcon
        class="absolute inset-y-0 left-4 text-sm h-full text-black/30"
      />
      <input
        type="text"
        placeholder="Search"
        class="w-full rounded-lg bg-black/10 px-8 py-1 outline-none appearance-none placeholder:text-black/30 text-black"
      />
      <SettingsIcon
        class="absolute inset-y-0 right-5 text-sm h-full text-black/30"
      />
    </div>

    <TabBar class="py-4" :items="items" :is-component-item="false"> </TabBar>
  </header>
</template>

<script setup lang="ts">
import NavBar from "./NavBar.vue";
import TabBar from "../Profile/TabBar.vue";
import SearchIcon from "~icons/tabler/search";
import SettingsIcon from "~icons/tabler/adjustments-horizontal";
const items = ["Primary", "General", "Requests"];
</script>
