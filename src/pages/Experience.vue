<script setup>
import EduItem from '../components/items/ExperienceItems/EduItem.vue';

import ExperienceItem from '../components/items/ExperienceItems/ExperienceItem.vue';
</script>

<template>
  <div class="wrapper">
    <div class="education-card">
      <h1>Education</h1>
      <EduItem />

    </div>
    <div class="experience-card">
      <h1>Experience</h1>
      <ExperienceItem />
    </div>
  </div>
</template>

<style scoped>
.wrapper {
  margin-left: 2rem;
  margin-right: 2rem;
  flex-wrap: wrap;
  gap: 20px;
}


.education-card {
  display: flex;
  flex-direction: column;
  align-items: left;
  margin-bottom: 2rem;
}

.experience-card {
  display: flex;
  flex-direction: column;
  align-items: left;
  margin-bottom: 2rem;
}

h1 {
  font-size: 2rem;
  font-weight: bold;
  font-family: Sigmar One,serif;
  margin-bottom: 1rem;
}
</style>