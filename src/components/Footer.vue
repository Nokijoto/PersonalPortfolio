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

const currentYear = new Date().getFullYear(); // Dynamically get the current year
</script>

<style scoped>
.footer {
  background-color: #B7A261; /* Tło stopki */
  color: var(--base-light-color); /* Kolor tekstu stopki */
  padding: 20px; /* Wewnętrzny odstęp */
  text-align: center; /* Wyśrodkowanie tekstu */
}

.footer-content {
  max-width: 100vw; /* Maksymalna szerokość stopki */
  margin: auto; /* Wyśrodkowanie stopki */
  height:1rem;
}

.footer a {
  color: white; /* Kolor linków */
  text-decoration: none; /* Brak podkreślenia */
}

.footer a:hover {
  text-decoration: underline; /* Podkreślenie linków po najechaniu */
}
</style>
