<script setup>
import NavBar from './components/NavBar.vue';
import HeaderSection from './components/HeaderSection.vue'
import About from './components/About.vue';
import skills from './components/skills.vue';
import Projects from './components/Projects.vue';
import Achievements from './components/Achievements.vue';
import ContactMe from './components/ContactMe.vue';
import footerPage from './components/footerPage.vue';
</script>

<template>
  <div class="bg-[var(--color-bg)] min-h-screen">
    <NavBar/>
    <HeaderSection/>
    <About/>
    <skills/>
    <Projects/>
    <Achievements/>
    <ContactMe/>
    <footerPage/>
  </div>
</template>
<!-- gsap -->
<style>
  ::-webkit-scrollbar{
    width: 8px;
    background-color: var(--color-bg);
  }
  ::-webkit-scrollbar-thumb{
    background: linear-gradient(to bottom, var(--color-primary), var(--color-secondary));
    border-radius: 20px;
  }
</style>
