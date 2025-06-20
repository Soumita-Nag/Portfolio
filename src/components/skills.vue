<template>
  <section class="text-white relative z-10">
    <div class="py-8 px-4 xl:px-16">
      <h2 class="text-4xl font-bold mb-10 text-left">
        My
        <span class="text-transparent bg-clip-text bg-gradient-to-r from-[var(--color-primary)] to-[var(--color-secondary)]">Skills</span>
      </h2>

      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-10">
        <div v-for="(group, index) in skillCategories" :key="index" class="space-y-6">
          <h3 class="text-2xl font-semibold" data-aos="fade-up">{{ group.title }}</h3>

          <!-- Skills -->
          <div v-for="skill in group.skills" :key="skill.id" class="mb-4" data-aos="fade-up">
            <div class="flex items-center justify-between">
              <span class="font-semibold md:w-[15%] w-[15%] uppercase">{{ skill.name }}</span>
              <div class="mt-2 h-1 mr-[10%] lg:w-[60%] w-[50%] bg-[#1f2f4b] rounded-full">
                <div class="h-1 rounded-full bg-gradient-to-r from-[var(--color-primary)] to-[var(--color-secondary)]" :style="`width: ${skill.width}`"></div>
              </div>
              <!-- <span class="font-semibold w-[8%] lg:w-[10%] text-transparent bg-clip-text bg-gradient-to-r from-[var(--color-primary)] to-[var(--color-secondary)]">{{ skill.width }}</span> -->
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
          title: "1. Programming & Scripting Languages",
          skills: [
            { id: 1, name: 'C', width: '85%' },
            { id: 2, name: 'C++', width: '90%' },
            { id: 3, name: 'Java', width: '80%' },
            { id: 4, name: 'Python', width: '70%' },
            { id: 5, name: 'JavaScript', width: '85%' },
            { id: 6, name: 'php', width: '80%' },
            { id: 7, name: 'sql', width: '85%' },
          ]
        },
        {
          title: "2. Web & Database Technologies",
          skills: [
            { id: 8, name: 'HTML', width: '95%' },
            { id: 9, name: 'CSS', width: '90%' },
            { id: 10, name: 'Tailwind CSS', width: '90%' },
            { id: 11, name: 'Vue.js', width: '90%' },
            { id: 12, name: 'Node.js', width: '90%' },
            { id: 13, name: 'Express.js', width: '90%' },
            { id: 14, name: 'MongoDB', width: '80%' },
            { id: 15, name: 'MySQL', width: '85%' },
          ]
        },
        {
          title: "3. Tools & Development Platforms",
          skills: [
            { id: 16, name: 'Git', width: '85%' },
            { id: 17, name: 'Postman', width: '75%' },
            { id: 18, name: 'GitHub', width: '85%' },
            { id: 19, name: 'VS Code', width: '90%' },
            { id: 20, name: 'Jupyter Notebook', width: '70%' }
          ]
        },
      ]
    };
  }
};
</script>

<style scoped>
</style>
