<script setup>
import { ref, shallowRef  } from 'vue';
import Header from './components/Header.vue';
import Profile from './components/Profile.vue';
import PageSwitcher from './components/items/PageSwitcher.vue';
import HomePage from './pages/HomePage.vue';
import Experience from './pages/Experience.vue';
import Projects from './pages/Projects.vue';
import Skills from './pages/Skills.vue';
import Contact from './pages/Contact.vue';
import Footer from './components/Footer.vue';
const selectedPage = shallowRef(HomePage);
const selectPage = (pageComponent) => {
  selectedPage.value = pageComponent;
};
</script>

<template>
  <header>
    <div class="wrapper">
      <Header />
    </div>
  </header>

  <main>
    <div class="container">
      <div class="column profile">
        <Profile />
      </div>
      <div class="column portfolio">
        <component :is="selectedPage" />
      </div>
      <div class="column pages">
        <PageSwitcher @change-page="selectPage" />
      </div>
    </div>
  </main>
  <Footer />
</template>

<style scoped>


header {
  line-height: 1.5;
  position: fixed;
  top: 2rem;
  left: 0;
  z-index: 1000;
  width: 100%;
  height: 2rem;
}
footer {
  position: fixed;
  bottom: 0;
  left: 0;
  z-index: 1000;
  width: 100%;
  height: 2rem;
}

.container {
  display: flex;
  justify-content: space-between;
  padding: 20px;
  margin-top: 100px;
  width: calc(100% - 40px);
}

.column {
  padding: 20px;
  border-radius: 5px ;
  width: auto;
}

.profile {
  margin-left: 2rem;
}

.portfolio {
  margin-left: 2rem;
  margin-right: 2rem;
  background-color: var(--base-light-color);
  border-radius: 10px;
  border: 3px solid #B7A261;
  width: 8vw;
  height: 40rem;
  flex: 0 0 100%;
}

.pages {
  margin-right: 5rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}

@media (max-width: 768px) {
  .container {
    flex-direction: column;
  }

  .column {
    margin: 10px 0;
    justify-content: center;
    align-items: center;
  }
}
</style>
