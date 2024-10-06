<script setup>
import SocialLinks from "@/components/items/ProfileItems/SocialLinks.vue";

defineProps({
  name: {
    type: String,
    required: true,
  },
  title: {
    type: String,
    required: true,
  },
  phone: {
    type: String,
    required: true,
  },
  email: {
    type: String,
    required: true,
  },
  location: {
    type: String,
    required: true,
  },
  birthdate: {
    type: String,
    required: true,
  },
});
const socialLinks = [
  { icon: 'fab fa-linkedin', url: import.meta.env.VITE_APP_LINKEDIN_URL },
  { icon: 'fab fa-github', url: import.meta.env.VITE_APP_GITHUB_URL },
];

</script>

<template>

  <div>
    <div class="contact-name">
      <h2>{{ name }}</h2>
    </div>
    <div class="contact-title">
      <h3>{{ title }}</h3>
    </div>
  </div>
    <SocialLinks :links="socialLinks" />
  <div class="contact-info">
    <div class="info-item" v-if="phone">
      <font-awesome-icon icon="phone" class="icon" /> {{ phone }}
    </div>
    <div class="info-item" v-if="email">
      <a :href="'mailto:' + email" class="email-link">
        <font-awesome-icon icon="envelope" class="icon" /> {{ email }}
      </a>
    </div>
    <div class="info-item" v-if="location">
      <font-awesome-icon icon="map-marker-alt" class="icon" /> {{ location }}
    </div>
    <div class="info-item" v-if="birthdate">
      <font-awesome-icon icon="birthday-cake" class="icon" /> {{ birthdate }}
    </div>
  </div>
</template>

<style scoped>

.contact-info {
  padding: 1rem;
  border-radius: 8px;
  background-color: #F9F6EA;
}

.info-item {
  display: flex;
  align-items: center;
  margin: 0.5rem;
  padding: 0.5rem;
  border-bottom: 1px solid #b59b56;
}

.icon {
  padding:0.5rem;
  margin-right: 0.5rem;
  margin-left: 0.5rem;
}

.contact-title {
  margin: 1rem auto;
  border-radius: 5px;
  border: 1px solid #b59b56;
  background-color: #f9f1d2;
  text-align: center;
  width: fit-content;
  padding: 0.2rem 0.5rem;
}
div.contact-title {
  justify-content: center;
}

.email-link {
  text-decoration: none;
  color: inherit;
  display: flex;
  align-items: center;
}
.email-link .icon {
  margin-left: 0.2rem;
}
</style>
