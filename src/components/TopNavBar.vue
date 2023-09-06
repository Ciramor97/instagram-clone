<template>
  <div
    class="lg:w-[27.5%] fixed top-0 px-4 py-2 flex justify-between shadow-sm border-b border-[##DBDBDB] bg-white"
    v-if="route.path === '/'"
  >
    <router-link to="/camera">
      <IconCamera class="text-xl" />
    </router-link>

    <router-link to="/">
      <LogoInstagram class="h-8 pt-1 w-24" />
    </router-link>

    <router-link to="/messages">
      <IconMessage class="text-xl" />
    </router-link>
  </div>
</template>

<script setup lang="ts">
// Icons
import IconCamera from "~icons/tabler/camera";
import IconMessage from "~icons/tabler/message-circle";
import LogoInstagram from "~icons/logos/instagram";
import { useRoute } from "vue-router";

const route = useRoute();
</script>
