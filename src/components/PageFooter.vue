<template>
  <footer class="footer mt-auto py-3">
    <div class="container">
      <div class="text-center">
        <hr />
        <div class="row">
          <div class="col" style="min-width: 300px">
            &copy; Copyright {{ getFullYear() }}.
          </div>
          <div class="col" style="min-width: 300px">
            <a href="https://myvet.uz">MyVet.Uz</a>
          </div>
          <div class="col" style="min-width: 300px">Все права защищены.</div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts">
function getFullYear() {
  const date = new Date();
  return date.getFullYear();
}
</script>
