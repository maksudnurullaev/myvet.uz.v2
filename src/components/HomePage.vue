<template>
  <!-- view-Home-->
  <div class="container">
    <template v-if="isDate(2022, 12, 21)">
      <home-page-action />
    </template>
    <template v-else>
      <home-page-default />
    </template>

    <home-page-carousel />
  </div>
</template>

<script setup lang="ts">
import HomePageCarousel from "@/components/HomePageCarousel.vue";
import HomePageAction from "@/components/HomePageAction.vue";
import HomePageDefault from "@/components/HomePageDefault.vue";

function isDate(year: number, month: number, day: number): boolean {
  const d = new Date(),
    cMonth = "" + (d.getMonth() + 1),
    cDay = "" + d.getDate(),
    cYear = d.getFullYear();
    return year <= cYear && month <= cMonth && day >= cDay;
}
</script>
