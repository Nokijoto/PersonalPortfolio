<script setup>


import GitIcon from '../../icons/ToolsIcons/GitIcon.vue';
import CsharpIcon from '../../icons/SkillsIcons/CSharpIcon.vue';
import MongoDbIcon from '../../icons/SkillsIcons/MongoDbIcon.vue';
import MariaDbIcon from '../../icons/SkillsIcons/MariaDbIcon.vue';
import PostgresSqlIcon from '../../icons/SkillsIcons/PostgresSqlIcon.vue';
import SqlServerIcon from '../../icons/SkillsIcons/SqlServerIcon.vue';
import LaravelIcon from '../../icons/SkillsIcons/LaravelIcon.vue';
import PhpIcon from '../../icons/SkillsIcons/PhpIcon.vue';

const skillsItems = [
  { label: 'Git', icon: GitIcon },
  { label: 'C#', icon: CsharpIcon },
  {label: 'Laravel', icon: LaravelIcon },
  { label: 'MongoDB', icon: MongoDbIcon },
  { label: 'MariaDB', icon: MariaDbIcon },
  { label: 'PostgreSQL', icon: PostgresSqlIcon },
  { label: 'SQL Server', icon: SqlServerIcon },
  { label: 'PHP', icon: PhpIcon },
];


</script>

<template>
  <div class="skills-container">
      <div class="skills-item" v-for="(item, index) in skillsItems" :key="index">
        <div class="skill-card">
          <component :is="item.icon" class="icon" />
        </div>
        <span>{{ item.label }}</span>
    </div>
  </div>
</template>

<style scoped>
.skills-container {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.icon {
  width: 30px;
  height: 30px;
}

.skills-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 10px;
}

.skill-card {
  border: 2px solid #B7A261;
  width: auto;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
}
</style>