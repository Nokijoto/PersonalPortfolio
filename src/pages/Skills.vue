<script setup>
import SkillItems from '../components/items/SkillsItems/SkillItems.vue';
import ToolsItems from '../components/items/SkillsItems/ToolsItems.vue';
</script>

<template>
  <div class="wrapper">
    <h1>Skills</h1>
    <SkillItems />
    <h1>Tools</h1>
    <ToolsItems />
  </div>
</template>

<style scoped>
h1 {
  font-size: 2rem;
  font-weight: bold;
  font-family: Sigmar One,serif;
  margin-bottom: 1rem;
}
.wrapper {
  display: flex;
  flex-direction: column;
  align-items: left;
  gap: 1rem;
  margin-left: 2rem;
  margin-right: 2rem;
}

</style>