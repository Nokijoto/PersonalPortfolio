<script setup>
import GithubIcon from "@/components/icons/ToolsIcons/GithubIcon.vue";
import DockerIcon from "@/components/icons/ToolsIcons/DockerIcon.vue";
import JiraIcon from "@/components/icons/ToolsIcons/JiraIcon.vue";
import PostmanIcon from "@/components/icons/ToolsIcons/PostmanIcon.vue";
import GitIcon from "@/components/icons/ToolsIcons/GitIcon.vue";
import PortainerIcon from "@/components/icons/ToolsIcons/PortainerIcon.vue";

const toolsItems = [
  { label: 'Git', icon: GitIcon },
  { label: 'Github', icon: GithubIcon },
  { label: 'Docker', icon: DockerIcon },
  { label: 'Jira', icon: JiraIcon },
  { label: 'Postman', icon: PostmanIcon },
  { label: 'Portainer', icon: PortainerIcon },
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



.tools-container {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;

}

.icon {
  width: 30px;
  height: 30px;
}

.tools-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 10px;
  text-align: center;
}

.tool-icon {
  border: 2px solid #B7A261;
  border-radius: 5%;
  padding: 1rem;
  width: auto;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
  box-shadow:  1px 1px 1px #FEF6DD,
  0 0 10px rgba(202, 192, 176, 0.8),
  0 0 20px rgba(189, 184, 160, 0.6);

}

.tool-icon .icon {
  width: 3rem;
  height: 3rem;
}
.tools-item span {
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