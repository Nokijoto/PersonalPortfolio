<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  imageSrc: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <img src="../../../assets/ProtfolioImages/portfolio.png" alt="Portfolio" class="portfolio-image">
</template>

<style scoped>
.portfolio-image {

  height: auto;
}
</style>