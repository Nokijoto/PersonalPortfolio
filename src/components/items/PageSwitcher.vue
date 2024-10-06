<script setup>

import { defineEmits,markRaw } from 'vue';
import AboutIcon from '../icons/IconAbout.vue';
import ExperienceIcon from '../icons/IconExperience.vue';
import ProjectsIcon from '../icons/IconProjects.vue';
import SkillsIcon from '../icons/IconSkills.vue';
import ContactIcon from '../icons/IconContact.vue';

import HomePage from '../../pages/HomePage.vue';
import Experience from '../../pages/Experience.vue';
import Projects from '../../pages/Projects.vue';
import Skills from '../../pages/Skills.vue';
import Contact from '../../pages/Contact.vue';

const emit = defineEmits(['change-page']);

const menuItems = [
  { label: 'About', icon: AboutIcon, component: markRaw(HomePage) },
  { label: 'Experience', icon: ExperienceIcon, component: markRaw(Experience) },
  { label: 'Projects', icon: ProjectsIcon, component: markRaw(Projects) },
  { label: 'Skills', icon: SkillsIcon, component: markRaw(Skills) },
  { label: 'Contact', icon: ContactIcon, component: markRaw(Contact) }
];

let selectedPage = HomePage;
const changePage = (component) => {
  emit('change-page', component);
  selectedPage.value = component;
};

</script>

<template>
  <div class="sidebar">
    <div class="menu-item" v-for="(item, index) in menuItems" :key="index"
         @click="changePage(item.component)"
         :class="{ active: selectedPage === item.component }">
      <component :is="item.icon" class="icon" />
      <span>{{ item.label }}</span>
    </div>
  </div>
</template>

<style scoped>
.sidebar {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 1rem;
  border-radius: 30px;
  width: auto;
  border: 3px solid #B7A261;
  background-color: var(--base-light-color);
  scale: 0.8;
}

.menu-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: #FDF8E2;
  border-radius: 10px;
  margin: 1rem 0;
  padding: 1rem;
  width: 100%;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  cursor: pointer;
  transition: background-color 0.3s;
}

.menu-item:hover {
  background-color: #F9F6EA;
}


.menu-item.active {
  background-color: #B7A261;
  color: #B7A261;
}

.menu-item span {
  margin-top: 0.5rem;
  font-size: 16px;
  color: #000;
}
</style>