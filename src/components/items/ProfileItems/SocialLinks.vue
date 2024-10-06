<script setup>
defineProps({
  links: {
    type: Array,
    required: true,
  },
});
</script>

<template>
  <div class="social-links">
    <a v-for="(link, index) in links" :key="index" :href="link.url" target="_blank">
      <i :class="link.icon"></i>
    </a>
  </div>
</template>

<style scoped>

.social-links {
  display: flex;
  justify-content: center;
  margin: 1rem 1rem 1rem 1rem;

}

.social-links a {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 2rem;
  height: 2rem;
  margin: 1rem;
  color: #b59b56;
  font-size: 24px;
  border-radius: 0.5rem;
  border: 1px solid var(--base-border-color);
  padding: 1rem;
}
.social-links i {
  font-size: 24px;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
}
</style>