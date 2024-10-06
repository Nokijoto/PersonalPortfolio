<template>
  <footer class="footer">
    <div class="footer-content">
      <p>&copy; {{ currentYear }} xxx. All Rights Reserved.</p>
<!--      <p>Designed by <a href="https://github.com/Vednidhi930">Vednidhi930</a></p>-->
    </div>
  </footer>
</template>

<script setup>
import { ref } from 'vue';

const currentYear = new Date().getFullYear();
</script>

<style scoped>
.footer {
  background-color: var(--color-five);
  color: var(--base-light-color);
  padding: 20px;
  text-align: center;
}

.footer-content {
  max-width: 100vw;
  margin: auto;
  height:1rem;
}

.footer a {
  color: var(--base-light-color);
  text-decoration: none;
}

.footer a:hover {
  text-decoration: underline;
}
</style>
