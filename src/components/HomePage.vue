<template>
  <!-- view-Home-->
  <div class="container">
    <h1 class="text-center mt-2 font-monospace">
      График работы: КРУГЛОСУТОЧНО - 24/7!
    </h1>

    <template v-if="isLessDate(2023, 1, 3)">
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

function isLessDate(year: number, month: number, day: number): boolean {
  return false;
  // const d = new Date(),
  //   cMonth = d.getMonth() + 1,
  //   cDay = d.getDate(),
  //   cYear = d.getFullYear();
  // if (year < cYear ){
  //   return true
  // } else if( month < cMonth ){
  //   return true
  // } else if ( day < cDay ) {
  //   return true
  // }
  // return false
}
</script>
