<script setup>
import { ref } from 'vue';
import PortfolioImage from "@/assets/ProtfolioImages/portfolio.png";
import Modal from "@/components/modals/ProjectModal.vue";

const projects = [
  {
    label: 'Strona Portfolio',
    languages: 'Vue JS, HTML, CSS, JavaScript, TypeScript',
    image: PortfolioImage,
    alt: 'Portfolio',
    link: '',
  },
];

const isModalVisible = ref(false);
const selectedProject = ref(null);

const openModal = (project) => {
  selectedProject.value = project;
  isModalVisible.value = true;
};

const closeModal = () => {
  isModalVisible.value = false;
  selectedProject.value = null;
};
</script>

<template>
  <div class="project-container">
    <div class="project-card" v-for="(project, index) in projects" :key="index" @click="openModal(project)">
      <div class="project-icon">
        <img :src="project.image" :alt="project.alt" class="image-icon">
      </div>
      <span class="project-name">{{ project.label }}</span>
    </div>
  </div>

  <Modal :isVisible="isModalVisible" :project="selectedProject" @close="closeModal"/>
</template>

<style scoped>

.project-container {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.project-card {
  border: 3px solid var(--base-border-color);
  padding: 20px;
  border-radius: 5px;
  text-align: center;
  cursor: pointer;
  background-color: var(--base-item-background-color);
}

.image-icon {
  width: 300px;
  height: 200px;
  border-radius: 5px;
  border: 3px solid var(--base-border-color);
}

.project-name {
  font-size: 16px;
  font-weight: bold;
  text-align: left;
  color: var(--base-dark-color);
}
</style>
