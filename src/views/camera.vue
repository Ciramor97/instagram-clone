<template>
  <div class="bg-black px-4 py-6 min-h-screen flex flex-col text-white">
    <Header />

    <div class="flex-grow"></div>

    <CenterMenu />

    <Picturer />

    <BottomOptions />
  </div>
</template>
<script setup lang="ts">
import Header from "../components/Camera/Header.vue";
import CenterMenu from "../components/Camera/CenterMenu.vue";
import BottomOptions from "../components/Camera/BottomOptions.vue";
import Picturer from "../components/Camera/Picturer.vue";
</script>
