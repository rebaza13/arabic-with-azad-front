<template>
  <button @click="toggleTheme" class="theme-switcher">
    Toggle Theme
  </button>
</template>

<script setup>
import { ref, watchEffect, onMounted } from 'vue';

// Create a reactive state to hold the current theme
const theme = ref('light');

// Create a function to toggle the theme
function toggleTheme() {
  theme.value = theme.value === 'light' ? 'dark' : 'light';
}

// 'onMounted' ensures this code only runs in the browser
onMounted(() => {
  // Now it's safe to access the 'document'
  watchEffect(() => {
    document.documentElement.setAttribute('data-theme', theme.value);
  });
});
</script>

<style lang="scss">
.theme-switcher {
  padding: 8px 16px;
  border-radius: 8px;
  cursor: pointer;
  
  // Use our theme variables for styling the button itself!
  background-color: var(--bg-light);
  color: var(--text-color);
  border: 1px solid var(--border);
  box-shadow: var(--shadow);
}
</style>