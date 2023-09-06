<template>
  <div class="pt-6 pb-20 px-4 w-full">
    <Header></Header>
    <div class="mt-6 space-y-4 divide-y divide-black/10">
      <Section title="Today"
        ><ActivityRow
          v-for="item in 3"
          :key="'today' + item"
          :image="`https://picsum.photos/id/${item + 100}/200/200`"
        ></ActivityRow
      ></Section>
      <Section title="This week" class="py-4"
        ><ActivityRow
          v-for="item in 10"
          :key="'today' + item"
          :image="`https://picsum.photos/id/${item + 100}/200/200`"
        ></ActivityRow
      ></Section>
    </div>
  </div>
</template>

<script setup lang="ts">
import Header from "../components/Activity/Header.vue";
import Section from "../components/Activity/Section.vue";
import ActivityRow from "../components/Activity/ActivityRow.vue";
</script>
