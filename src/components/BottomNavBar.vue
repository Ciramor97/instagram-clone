<template>
  <div
    v-if="!filteredPages.includes(route.path)"
    class="lg:w-[27.5%] fixed bottom-0 px-4 py-2 flex justify-around shadow-sm border-t border-[##DBDBDB] bg-white items-center text-2xl"
  >
    <router-link to="/">
      <IconHome :filled="route.path == '/'" />
    </router-link>

    <router-link to="/explore">
      <IconSearchAlt />
    </router-link>

    <IconPlusAlt class="cursor-pointer" />

    <router-link to="/activity">
      <IconHeartAlt class="text-xl" />
    </router-link>

    <router-link to="/profile">
      <StoryBox avatar="" size="xs" :show-circle="false" />
    </router-link>
  </div>
</template>

<script setup lang="ts">
// Icons
import IconHome from "./Icons/Home.vue";
import IconSearchAlt from "~icons/tabler/search";
import IconPlusAlt from "~icons/tabler/circle-plus";
import IconHeartAlt from "~icons/tabler/heart";

import StoryBox from "./Story/Box.vue";

const filteredPages = ["/messages", "/camera"];

import { useRoute } from "vue-router";

const route = useRoute();
</script>
