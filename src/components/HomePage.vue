<template>
  <!-- view-Home-->
  <div class="container">
    <!-- Цитаты -->
    <div class="mt-2 mb-2">
      <div class="card text-dark bg-light">
        <div class="card-body">
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
        </div>
      </div>
    </div>
    <hr />
    <!-- <div class="container"> -->
    <home-page-carousel />
    <!-- </div> -->
    <h4>Полезные статьи</h4>
    <div class="row">
      <div class="col">
        <div class="card border-primary mb-3" style="min-width: 300px">
          <div class="card-header">Наша миссия</div>
          <div class="card-body text-primary">
            <h5 class="card-title">Primary card title</h5>
            <p class="card-text">
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </p>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card border-secondary mb-3" style="min-width: 300px">
          <div class="card-header">Наши цели</div>
          <div class="card-body text-secondary">
            <h5 class="card-title">Secondary card title</h5>
            <p class="card-text">
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col">
        <div class="card border-success mb-3" style="min-width: 300px">
          <div class="card-header">Header</div>
          <div class="card-body text-success">
            <h5 class="card-title">Success card title</h5>
            <p class="card-text">
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </p>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card border-danger mb-3" style="min-width: 300px">
          <div class="card-header">Header</div>
          <div class="card-body text-danger">
            <h5 class="card-title">Danger card title</h5>
            <p class="card-text">
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col">
        <div class="card border-warning mb-3" style="min-width: 300px">
          <div class="card-header">Header</div>
          <div class="card-body">
            <h5 class="card-title">Warning card title</h5>
            <p class="card-text">
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </p>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card border-info mb-3" style="min-width: 300px">
          <div class="card-header">Header</div>
          <div class="card-body">
            <h5 class="card-title">Info card title</h5>
            <p class="card-text">
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col">
        <div class="card border-light mb-3" style="min-width: 300px">
          <div class="card-header">Header</div>
          <div class="card-body">
            <h5 class="card-title">Light card title</h5>
            <p class="card-text">
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </p>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card border-dark mb-3" style="min-width: 300px">
          <div class="card-header">Header</div>
          <div class="card-body text-dark">
            <h5 class="card-title">Dark card title</h5>
            <p class="card-text">
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import HomePageCarousel from "@/components/HomePageCarousel.vue";
</script>
