<template>
  <section class="text-white mt-10 relative z-10" id="skills">
    <div class="py-8 px-4 xl:px-16">
      <h2 class="text-4xl font-bold mb-10 text-left">
        My
        <span class="text-transparent bg-clip-text bg-gradient-to-r from-[var(--color-primary)] to-[var(--color-secondary)]">Skills</span>
      </h2>

      <div class="grid md:grid-cols-2 gap-10">
        <div v-for="(group, index) in skillCategories" :key="index" class="space-y-6">
          <h3 class="text-2xl font-semibold" data-aos="fade-up">{{ group.title }}</h3>

          <!-- Optional Subtitle like Frontend/Backend -->
          <template v-if="group.subtitle">
            <p class="font-semibold" data-aos="fade-up">🔸 {{ group.subtitle }}</p>
          </template>

          <!-- Skills -->
          <div v-for="skill in group.skills" :key="skill.id" class="mb-4" data-aos="fade-up">
            <div class="flex items-center justify-between">
              <h4 class="font-semibold uppercase">{{ skill.name }}</h4>
              <span class="text-xl font-bold">{{ skill.width }}</span>
            </div>
            <div class="mt-2 h-1 w-full bg-[#131d30] rounded-full">
              <div class="h-1 rounded-full bg-[var(--color-primary)]" :style="`width: ${skill.width}`"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      skillCategories: [
        {
          title: "1. Programming Languages",
          skills: [
            { id: 1, name: 'C', width: '85%' },
            { id: 2, name: 'C++', width: '85%' },
            { id: 3, name: 'Java', width: '80%' },
            { id: 4, name: 'Python', width: '70%' },
            { id: 5, name: 'JavaScript', width: '85%' },
            { id: 6, name: 'PHP', width: '75%' }
          ]
        },
        {
          title: "2. Web Development (Frontend)",
          skills: [
            { id: 7, name: 'HTML', width: '90%' },
            { id: 8, name: 'CSS', width: '80%' },
            { id: 9, name: 'Tailwind CSS', width: '75%' },
            { id: 10, name: 'JavaScript', width: '85%' },
            { id: 11, name: 'Vue.js', width: '80%' }
          ]
        },
        {
          title: "3. Web Development (Backend)",
          skills: [
            { id: 12, name: 'Node.js', width: '70%' },
            { id: 13, name: 'Express.js', width: '70%' },
            { id: 14, name: 'PHP', width: '75%' }
          ]
        },
        {
          title: "4. Databases",
          skills: [
            { id: 15, name: 'MySQL', width: '80%' },
            { id: 16, name: 'MongoDB', width: '70%' }
          ]
        },
        // {
        //   title: "5. Developer Tools & Platforms",
        //   skills: [
        //     { id: 17, name: 'Git', width: '85%' },
        //     { id: 18, name: 'GitHub', width: '85%' },
        //     { id: 19, name: 'Postman', width: '75%' },
        //     { id: 20, name: 'VS Code', width: '90%' },
        //     { id: 21, name: 'Jupyter Notebook', width: '70%' }
        //   ]
        // }
      ]
    };
  }
};
</script>

<style scoped>
/* Tailwind handles styling */
</style>
