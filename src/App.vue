<template>
  <div class="lg:w-[27.5%] relative mx-auto min-h-screen">
    <TopNavBar />
    <Layout>
      <RouterView />
    </Layout>
    <BottomNavBar />
  </div>
</template>

<script setup lang="ts">
import TopNavBar from "./components/TopNavBar.vue";
import BottomNavBar from "./components/BottomNavBar.vue";
import Layout from "./components/Layout.vue";

import { useRouter } from "vue-router";

const router = useRouter();

router.beforeEach(() => {
  window.scrollTo({
    top: 0,
    behavior: "smooth",
  });
});
</script>

<style scoped></style>
