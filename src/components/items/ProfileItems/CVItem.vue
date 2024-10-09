<script setup>
import cv from '@/assets/cv/cv.pdf'; // Importuj plik PDF
</script>

<template>
  <div>
    <a :href="cv" download class="view-resume">Download CV</a>
  </div>
</template>

<style scoped>
.view-resume {
  margin-top: 1rem;
  padding: 0.5rem 1.5rem;
  background-color: var(--base-item-background-color);
  color: var(--color-four);
  border: 0.2rem solid var(--base-border-color);
  border-radius: 0.5rem;
  cursor: pointer;
  font-weight: bold;
  text-decoration: none;
  display: inline-block;
}
</style>