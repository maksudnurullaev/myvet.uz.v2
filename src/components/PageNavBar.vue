<script setup lang="ts">
import { reactive, ref } from "vue";

const navTogglerIcon = ref<HTMLElement | null>(null);

const resources = reactive({
  MainMenuBar: [
    { path: "/", title: "Главная" },
    { path: "/ourservices", title: "Услуги и цены" },
    { path: "/login", title: "Вход" },
    { path: "/about", title: "О нас" },
  ],
});

// function menuClicked(myArg: object) {
function menuClicked() {
  if (navTogglerIcon.value?.offsetParent) {
    navTogglerIcon.value.click(); // close navigation menu for mobile view
  }
}
</script>

<template>
  <!-- Responsive navbar-->
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark sticky-top">
    <div class="container">
      <a class="navbar-brand" href="https://myvet.uz">MyVet.Uz</a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon" ref="navTogglerIcon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
          <li
            class="nav-item"
            v-for="nav in resources.MainMenuBar"
            :key="nav.path"
          >
            <router-link
              class="nav-link"
              :to="nav.path"
              active-class="active"
              v-on:click="menuClicked"
              >{{ nav.title }}
            </router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style scoped>
.navbar {
  background-color: #14266e !important;
}
</style>
