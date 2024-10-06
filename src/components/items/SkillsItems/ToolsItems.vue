<script setup>
import GithubIcon from "@/components/icons/ToolsIcons/GithubIcon.vue";
import DockerIcon from "@/components/icons/ToolsIcons/DockerIcon.vue";
import JiraIcon from "@/components/icons/ToolsIcons/JiraIcon.vue";
import PostmanIcon from "@/components/icons/ToolsIcons/PostmanIcon.vue";

const toolsItems = [
  { label: 'Github', icon: GithubIcon },
  { label: 'Docker', icon: DockerIcon },
  { label: 'Jira', icon: JiraIcon },
  { label: 'Postman', icon: PostmanIcon },
  // { label: '', icon: },
];
</script>

<template>
  <div class="tools-container">
    <div class="tools-item" v-for="(item, index) in toolsItems" :key="index">
      <div class="tool-card" @click="openUrl(item.url)">
        <div class="tool-icon">
          <component :is="item.icon" class="icon" />
        </div>
        <span>{{ item.label }}</span>
      </div>
    </div>
  </div>
</template>

<style scoped>
*{
  border : 1px solid red;
}

.tools-container {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.tools-item {
  width: auto;
  height: auto;
  border-radius: 10px;
  padding: 20px;
  max-width: auto;
  flex: 1;
  min-width: auto;
  background-color: #ffffff;
}

.tool-icon {
  border: 2px solid #B7A261;
  width: auto;
  align-items: center;
  padding: 0.5rem 0.5rem 0.5rem 0.5rem;
  justify-content: center;
  gap: 10px;
  border-radius: 1rem;
}
.tool-icon .icon {
  width: 3rem;
  height: 3rem;
}
.tools-item span {
  font-size: 16px;
  color: #000;
  justify-content: center;
}


.tool-card span {
  justify-content: center;
}

.icon {
  width: 30px;
  height: 30px;
}
</style>