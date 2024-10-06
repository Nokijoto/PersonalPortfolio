<script setup>
import ProjectItem from '../components/items/ProjectItems/ProjectItem.vue';
</script>

<template>
  <div class="wrapper">
    <h1>Projects</h1>
    <ProjectItem />
  </div>
</template>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: column;
  align-items: left;
  gap: 1rem;
  margin-left: 2rem;
  margin-right: 2rem;
}

h1 {
  font-size: 2rem;
  font-weight: bold;
  font-family: Sigmar One,serif;
  margin-bottom: 1rem;
}
</style>