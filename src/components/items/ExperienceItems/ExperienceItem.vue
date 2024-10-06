<script setup>

</script>

<template>
  <div class="experience-container">
    <div class="experience-card">
      <div class="image-card">
          <img src="https://media.licdn.com/dms/image/v2/D4E0BAQGM4_sDTB1s3g/company-logo_200_200/company-logo_200_200/0/1716448871580?e=1736380800&v=beta&t=fSyt8OdVKhdmHwwHISF791Ur4oim_G7u8uiZ9CHVm80" alt="Cogniforge AI">
      </div>
      <div class="content-card">
        <p class="Company"><b>Company:</b> Cogniforge AI </p>
        <h3 class="Role"><b>Role:</b> Backend Developer · Intern</h3>
        <p class="Duration"><b>Duration:</b> May / 2024 - October / 2024</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
}

.experience-container {
  display: inline;
  flex-wrap: wrap;
  width: auto;
  gap: 20px;
}

.experience-card {
  padding-left: 1rem;
  display: flex;
  align-items: center;
  border: 2px solid var(--base-border-color);
  border-radius: 10px;
  max-width: auto;
  background-color: var(--base-background-color);
  padding: 1rem;
  text-align: left;
}

.image-card {
  text-align: center;
  max-width: 100%;
  width: 100px;
  height: 100px;
  border-radius: 20%;
  overflow: hidden;
  margin-right: 20px;
  border: 2px solid var(--base-border-color);
}

.image-card {
  max-width: 100%;
  text-align: center;
}

img {
  max-width: 100%;
  height: auto;
}
.content-card {
  display: flex;
  flex-direction: column;
  justify-content: center;

}

.Company, .Role, .Duration {
  margin-left: 0.5rem;
}
.Company {
  font-size: 16px;
  color: var(--base-dark-color);
}

.Role {
  font-size: 16px;
  color: var(--base-dark-color);
}

.Duration {
  font-size: 16px;
    color: var(--base-dark-color);

}
b{
  font-weight: bold;
  margin-right: 0.5rem;
}
</style>
