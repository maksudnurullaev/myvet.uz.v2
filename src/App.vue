<script setup lang="ts">
import PageNavBar from "./components/PageNavBar.vue";
import PageFooter from "./components/PageFooter.vue";
</script>

<template>
  <page-nav-bar />
  <router-view />
  <page-footer />
</template>
