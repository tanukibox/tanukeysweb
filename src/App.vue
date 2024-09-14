<script setup lang="ts">
import { RouterView } from 'vue-router'

const currentYear = new Date().getFullYear();

</script>

<template>
  <RouterView />

  <footer class="footer">
    <div class="content has-text-centered">
      <p>
        <strong>Tanukeys</strong> is a product by <a href="https://gitlab.com/tanukibox">TanukiBox</a>. All rights
        reserved © {{ currentYear }}.
      </p>
    </div>
  </footer>
</template>

<style>
@import "https://cdn.jsdelivr.net/npm/bulma@1.0.2/css/bulma.min.css";
</style>
