<script setup>
import ThemeSwitcher from './items/HeaderItems/ThemeSwitcher.vue'
import PortfolioHeader from './items/HeaderItems/PortfolioHeader.vue'
</script>

<template>
  <header class="header">
    <div class="logo">
      <PortfolioHeader />
    </div>
    <div class="theme-switcher">
      <ThemeSwitcher />
    </div>
  </header>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
}

.logo h1 {
  font-family: 'Arial', sans-serif;
  color: #b59b56;
  font-size: 24px;
  font-weight: bold;
  text-transform: uppercase;
  margin-left: 25rem;
}

.theme-switcher {
  font-size: 24px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
