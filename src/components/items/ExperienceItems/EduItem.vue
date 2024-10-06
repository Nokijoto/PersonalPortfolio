<script setup>

</script>

<template>
  <div class="education-container">
    <div class="education-card">
      <p class="years">2021 - 2025</p>
      <h3 class="degree">B.Tech ( IT ) from CSPIT, CHARUSAT</h3>
      <p class="cgpa">9.18 CGPA till 6th Sem</p>
    </div>
    <div class="education-card">
      <p class="years">2017 - 2021</p>
      <h3 class="degree">B.Tech ( IT ) from CSPIT, CHARUSAT</h3>
      <p class="cgpa">9.18 CGPA till 6th Sem</p>
    </div>
  </div>
</template>

<style scoped>
.education-container {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.education-card {
  border: 2px solid #B7A261;
  border-radius: 10px;
  padding: 20px;
  max-width: 400px;
  flex: 1;
  min-width: 200px;
  background-color: #ffffff;
}

.years {
  font-size: 14px;
  color: #333;
  margin-bottom: 10px;
}

.degree {
  font-weight: bold;
  font-size: 16px;
  color: #000;
  margin: 5px 0;
}

.cgpa {
  font-size: 14px;
  color: #555;
}
</style>
