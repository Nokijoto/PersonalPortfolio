<script setup>
import { defineProps, defineEmits } from 'vue';

const props = defineProps({
  isVisible: {
    type: Boolean,
    required: true
  },
  project: {
    type: Object,
    required: true
  }
});

const emit = defineEmits(['close']);

const closeModal = () => {
  emit('close');
};
</script>

<template>
  <div class="modal" v-if="isVisible">
    <div class="modal-content">
      <span class="close" @click="closeModal">&times;</span>
      <div class="image-container">
        <img :src="project.image" alt="Project Image">
      </div>
      <h2>{{ project.label }}</h2>
      <p>{{ project.languages }}</p>
      <p>More details about the project...</p>
      <a :href="project.link" target="_blank">Project Link</a>
    </div>
  </div>
</template>

<style scoped>
.modal {
  display: flex;
  justify-content: center;
  align-items: center;
  position: fixed;
  z-index: 1000;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.7);
  transition: opacity 0.3s ease;
}

.modal-content {
  background-color: white;
  padding: 20px;
  border-radius: 8px;
  text-align: center;
  max-width: 90%;
  max-height: 90%;
  overflow: auto;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.2);
  position: relative;
}


.close {
  cursor: pointer;
  font-size: 24px;
  position: absolute;
  right: 20px;
  top: 20px;
  color: #333;
  background-color: rgba(255, 255, 255, 0.8);
  border-radius: 50%;
  padding: 5px;
  z-index: 1010;
  transform: translate(50%, -50%);
}

.image-container {
  margin: 20px 0;
}

img {
  width: 100%;
  height: auto;
  max-width: 900px;
  max-height: 400px;
}
</style>
