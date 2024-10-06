<script setup>
import PortfolioImage from "@/components/icons/Project/PortfolioImage.vue";

const projects = [
  { label: 'Strona Portfolio', icon: PortfolioImage, languages: 'Vue JS, HTML, CSS, JavaScript, TypeScript' },
];
</script>

<template>
  <div class="project-container">
    <div class="project-card" v-for="(project, index) in projects" :key="index">
      <div class="project-icon">
        <component :is="project.icon" class="image-icon" />
      </div>
      <span class="project-name">{{ project.label }}</span>
      <span class="project-languages">{{ project.languages }}</span>
    </div>
  </div>
</template>

<style scoped>
.project-container {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}
.project-card {
  border: 1px solid #ccc; /* Example border for the card */
  padding: 20px; /* Example padding */
  border-radius: 5px; /* Example border-radius */
  text-align: center; /* Center text */
}
.image-icon {
  width: 50px; /* Example size for the icon */
  height: 50px; /* Example size for the icon */
}
</style>
