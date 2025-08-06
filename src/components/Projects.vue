<template>
  <section id="projects" class="text-white select-none relative z-10 pt-20">
    <h2 class="text-4xl font-bold mb-4 px-4 xl:pl-16">
      My <span class="text-transparent bg-clip-text bg-gradient-to-r from-[var(--color-primary)] to-[var(--color-secondary)]">Projects</span>
    </h2>
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 items-stretch py-8 px-4 xl:gap-8 sm:py-16 xl:px-16">
      <div v-for="project in projects" :key="project.name" data-aos="flip-left">
        <div v-if="project.frontView" data-aos="flip-left" class="bg-[#111a3e]/80 transition-all rounded-2xl shadow-lg flex flex-col justify-between">
        <div class="px-6 pt-6">
          <div class="flex justify-between items-center mb-4">
            <h3 class="text-transparent bg-clip-text bg-gradient-to-r from-[var(--color-primary)] to-[var(--color-secondary)] font-bold text-2xl">{{ project.name }}</h3>
            <span @click="project.frontView=false" class="text-[var(--color-primary)] font-semibold text-xl border border-[var(--color-primary)] px-4 rounded-lg hover:cursor-pointer hover:bg-[var(--color-primary)] hover:text-white">i</span>
          </div>
          <div class="w-full flex justify-center mb-4">
            <img :src="project.image" alt="project image" class="rounded-lg max-h-48 object-contain" />
          </div>
          <div class="flex flex-wrap justify-center gap-2 mb-4">
            <span v-for="tech in project.technologies" :key="tech" class="bg-[var(--color-primary)]/20 text-[var(--color-primary)] text-xs font-medium px-2 py-1 rounded-full">
              {{ tech }}
            </span>
          </div>
        </div>
        <div class="flex justify-between items-center px-6 py-4 border-t border-gray-600/40">
          <a :href="project.liveLink" target="_blank" class="text-sm text-white bg-gradient-to-r from-[var(--color-primary)] to-[var(--color-secondary)] hover:scale-105 font-semibold px-4 py-2 rounded-md transition">Live Demo</a>
          <a :href="project.githubRepo" target="_blank" class="text-sm text-[var(--color-primary)] border border-[var(--color-primary)] hover:bg-[var(--color-primary)] hover:text-white font-semibold px-4 py-2 rounded-md transition">GitHub Repo</a>
        </div>
        </div>
        <div v-else data-aos="flip-left" @click="project.frontView=true" class="cursor-pointer bg-[#111a3e]/80 transition-all rounded-2xl shadow-lg flex flex-col justify-between">
        <div class="px-6 pt-6 min-h-98">
          <div class="flex justify-between items-center mb-4">
            <h3 class="text-transparent bg-clip-text bg-gradient-to-r from-[var(--color-primary)] to-[var(--color-secondary)] font-bold text-2xl">{{ project.name }}</h3>
            
          </div>
          <div class="w-full mb-4">
            {{ project.description }}
          </div>
        </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';
import askhiveImg from '@/assets/askhive.png';
import codenameImg from '@/assets/codename.png';
import expensetracker from '@/assets/expensetracker.png';

var frontView=ref(true);
const projects = ref([
  {
    name: "AskHive",
    liveLink: "https://askhive.soumita.xyz",
    githubRepo: "https://github.com/Soumita-Nag/QueryService",
    image: askhiveImg,
    description: "AskHive is a dynamic query management web application designed to streamline the process of asking, answering, and managing user-submitted questions. Built with Vue.js on the frontend and Node.js with MongoDB Atlas on the backend, it provides a seamless platform for real-time interaction between users and admins. Users can post queries across various categories like programming, history, science, and more, while admins can review, filter, and respond to them from a dedicated dashboard. The platform ensures transparency and encourages knowledge-sharing in a structured environment. Security and scalability are key focuses, with proper authentication, environment-based configuration, and deployment handled via Render and GitHub integration. AskHive is ideal for educational platforms, support centers, or any community that values organized knowledge exchange.",
    technologies: ['Vue JS', 'Node JS', 'MongoDB'],
    frontView:true,
  },
  {
    name: "CodeName",
    liveLink: "https://codename.soumita.xyz/",
    githubRepo: "https://github.com/Soumita-Nag/CodeName",
    image: codenameImg,
    description: "Codename Game is a real-time, web-based multiplayer game inspired by the popular party game Codenames. It’s built using Vue.js for the frontend and Firebase (Realtime Database + Firestore) for backend functionality and live synchronization between players. Players can join or create rooms, choose roles like Spymaster or Operative, and engage in a competitive word-association challenge. The Spymaster sees the color-coded word grid, while team members try to guess the correct words based on given hints. The game supports real-time state updates across all clients for an engaging and interactive experience. With its sleek UI, role-based interaction, and Firebase-powered live updates, Codename Game delivers an exciting and collaborative environment ideal for both fun and brain-teasing gameplay.",
    technologies: ['Vue JS', 'Firebase'],
    frontView:true,
  },
  {
    name: "Expense Tracker",
    liveLink: "https://expense-tracker.soumita.xyz/",
    githubRepo: "https://github.com/Soumita-Nag/ExpenseTracker",
    image: expensetracker,
    description: "The Expense Tracker is a simple yet powerful web application designed to help users manage and monitor their daily expenses effectively. Built using Vue.js for the frontend and Node.js with MongoDB for the backend, the app provides a seamless experience for recording and categorizing financial transactions. Users can add income or expenses, assign categories, and view summaries or trends over time. The dashboard provides real-time updates and a clean visualization of financial data, making budgeting easier and more intuitive. This project emphasizes practical personal finance management while demonstrating full-stack development skills using modern web technologies.",
    technologies: ['Vue JS', 'Tailwind CSS'],
    frontView:true,
  },
]);
</script>

<style scoped>
</style>
