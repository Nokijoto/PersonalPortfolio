<script setup>


import CsharpIcon from '../../icons/SkillsIcons/CSharpIcon.vue';
import DotNetIcon from '../../icons/SkillsIcons/DotNetIcon.vue';
import MongoDbIcon from '../../icons/SkillsIcons/MongoDbIcon.vue';
import MariaDbIcon from '../../icons/SkillsIcons/MariaDbIcon.vue';
import PostgresSqlIcon from '../../icons/SkillsIcons/PostgresSqlIcon.vue';
import SqlServerIcon from '../../icons/SkillsIcons/SqlServerIcon.vue';
import LaravelIcon from '../../icons/SkillsIcons/LaravelIcon.vue';
import PhpIcon from '../../icons/SkillsIcons/PHPIcon.vue';
import JsIcon from "@/components/icons/SkillsIcons/JsIcon.vue";
import TypescriptIcon from "@/components/icons/SkillsIcons/TypescriptIcon.vue";
import AngularIcon from "@/components/icons/SkillsIcons/AngularIcon.vue";
import MarkdownIcon from "@/components/icons/SkillsIcons/MarkdownIcon.vue";

const skillsItems = [
  { label: 'C#', icon: CsharpIcon },
  { label: '.Net', icon: DotNetIcon },
  {label: 'Laravel', icon: LaravelIcon },
  { label: 'PHP', icon: PhpIcon },
  { label: 'MongoDB', icon: MongoDbIcon },
  { label: 'MariaDB', icon: MariaDbIcon },
  { label: 'PostgreSQL', icon: PostgresSqlIcon },
  { label: 'SQL Server', icon: SqlServerIcon },
  { label: 'JavaScript', icon: JsIcon },
  { label: 'TypeScript', icon: TypescriptIcon },
  { label: 'Angular', icon: AngularIcon },
  { label: 'Markdown', icon: MarkdownIcon },
];


</script>

<template>
  <div class="skills-container">
      <div class="skills-item" v-for="(item, index) in skillsItems" :key="index">
        <div class="skill-card">
          <div class="skill-icon">
            <component :is="item.icon" class="icon" />
          </div>
          <span class="skill-name">{{ item.label }}</span>
        </div>
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
  text-align: center;
}

.skill-icon {
  border: 2px solid var(--base-border-color);
  border-radius: 5%;
  padding: 1rem;
  width: auto;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
  box-shadow:  1px 1px 1px var(--base-background-color),
  0 0 10px rgba(202, 192, 176, 0.8),
  0 0 20px rgba(189, 184, 160, 0.6);

}

.skill-icon .icon {
  width: 3rem;
  height: 3rem;
}
.skills-item span {
  font-size: 16px;
  color: var(--base-dark-color);
  justify-content: center;
  width: 100%;
  text-align: center;
}


.skill-card{
  justify-content: center;
  align-items: center;
}
.skill-card .skill-name {
  text-align: center;
}

.icon {
  width: 30px;
  height: 30px;
}
</style>