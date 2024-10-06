<script setup>
import ProfilePicture from './items/ProfileItems/ProfilePicture.vue';
import ContactInfo from './items/ContactInfo.vue';
import SocialLinks from './items/ProfileItems/SocialLinks.vue';

const imageSrc = import.meta.env.VITE_APP_PROFILE_PICTURE_URL;
const name = import.meta.env.VITE_APP_USER_NAME;
const title = import.meta.env.VITE_APP_USER_TITLE;
const phone = import.meta.env.VITE_APP_USER_PHONE;
const email = import.meta.env.VITE_APP_USER_EMAIL;
const location = import.meta.env.VITE_APP_USER_LOCATION;
const birthdate = import.meta.env.VITE_APP_USER_BIRTHDATE;


</script>

<template>
  <div class="user-profile">
    <ProfilePicture :imageSrc="imageSrc" />
    <ContactInfo
        :name="name"
        :title="title"
        :phone="phone"
        :email="email"
        :location="location"
        :birthdate="birthdate"
    />
    <button class="view-resume">View Resume</button>
  </div>
</template>

<style scoped>
.user-profile {
  text-align: center;
  padding: 2rem;
  background-color: var(--base-light-color);
  border-radius: 1rem;
  box-shadow: 0 1rem 0.5rem rgba(0, 0, 0, 0.1);
  border: 3px solid var(--base-border-color);
  height: auto;
  width: auto;
  scale: 0.9;
}

.view-resume {
  margin-top: 1rem;
  padding: 0.5rem 1.5rem;
  background-color: #E0CE93;
  color: #403D22;
  border: 0.2rem solid var(--base-border-color);
  border-radius: 0.5rem;
  cursor: pointer;
  font-weight: bold;
}
</style>