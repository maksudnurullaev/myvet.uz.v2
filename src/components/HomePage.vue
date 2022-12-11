<template>
  <!-- view-Home-->
  <div class="container">
    <!-- <home-page-action /> -->
    <!-- Цитаты -->
    <div class="mt-2 mb-2">
      <div class="card text-dark bg-light">
        <div class="card-body">
          <img
            src="/photos/Logo_horizontal_small.jpg"
            class="rounded float-start me-2 d-none d-lg-block"
          />
          <h5 class="card-title">Мысли о животных</h5>
          <p class="card-text">
            <span class="font-italic">
              Животные суть не что иное, как прообразы наших добродетелей и
              пороков, блуждающих пред нашим взором, призраки наших душ...
            </span>
          </p>
          <a
            href="https://ru.wikipedia.org/wiki/%D0%93%D1%8E%D0%B3%D0%BE,_%D0%92%D0%B8%D0%BA%D1%82%D0%BE%D1%80"
            target="_blank"
            class="card-link"
            >© В. Гюго</a
          >
          <br /><br />
          <a
            href="tel:+998909653034"
            type="button"
            class="btn btn-primary bt-3 btn-lg"
            id="liveAlertBtn"
          >
            Звоните на номер: (90) 965 30 34
          </a>
        </div>
      </div>
    </div>
    <!-- <div class="container"> -->
    <home-page-carousel />
    <!-- </div> -->
  </div>
</template>

<script setup lang="ts">
import HomePageCarousel from "@/components/HomePageCarousel.vue";
import HomePageAction from "@/components/HomePageAction.vue";
</script>
