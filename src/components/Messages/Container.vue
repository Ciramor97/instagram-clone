<template>
  <div class="px-4 pb-4 flex flex-col space-y-3">
    <ContainerRow
      v-for="person in randomizeData"
      :key="person.user.nickname"
      :avatar="person.image"
      :username="person.user.nickname"
    ></ContainerRow>
  </div>
</template>

<script setup lang="ts">
import ContainerRow from "./ContainerRow.vue";
// import data from "../../data/index";
import { computed } from "vue";
import useDataStore from "../../store/data";

const store = useDataStore();
const randomizeData = computed(() => store.getRandomizedData);
</script>
