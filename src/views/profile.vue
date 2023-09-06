<template>
  <Header name="Roma_dev"></Header>
  <ProfileStats></ProfileStats>
  <ProfileInfos></ProfileInfos>
  <Buttons></Buttons>
  <Highlights></Highlights>
  <TabBar :items="items" isComponentItem></TabBar>
  <Container type="profile" class="pb-16" />
</template>
<script setup lang="ts">
import Header from "../components/Profile/Header.vue";
import ProfileStats from "../components/Profile/Stats.vue";
import ProfileInfos from "../components/Profile/Infos.vue";
import Buttons from "../components/Profile/Buttons.vue";
import Highlights from "../components/Profile/Highlights.vue";
import TabBar from "../components/Profile/TabBar.vue";
import Container from "../components/Explore/Container.vue";
//icons
import IconGrid from "~icons/tabler/layout-grid";
import IconVideo from "~icons/tabler/video";
import IconTag from "~icons/tabler/tag";
const items = [IconGrid, IconVideo, IconTag];
</script>
