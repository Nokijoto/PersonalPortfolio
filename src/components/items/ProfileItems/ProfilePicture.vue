<script setup>
defineProps({
  imageSrc: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="profile-picture">
    <img :src="imageSrc" alt="Profile Picture" />
  </div>
</template>

<style scoped>
.profile-picture {
  margin-bottom: -6rem;
  transform: translate(0, -50%);
}

img {
  border: 4px solid var(--base-border-color);
  border-radius: 7.5%;
}
.profile-picture img {
  width: 200px;
  height: 200px;
}
</style>