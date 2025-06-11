<template>
  <section class="w-full py-20 px-5 sm:px-8 md:px-12 lg:px-8 max-w-screen-lg xl:max-w-screen-xl mx-auto" data-aos="zoom-in-up">
    <div class="grid lg:grid-cols-2 gap-10 xl:gap-14 pt-10 max-w-3xl lg:max-w-none mx-auto">
      <div class="lg:py-6">
        <!-- Heading -->
        <div class="text-center lg:text-left">
          <h1 class="text-white font-bold text-4xl md:text-5xl lg:text-6xl">
            Hi, I'm 
            <span class="text-transparent bg-clip-text bg-gradient-to-r from-[var(--color-primary)] to-pink-500">
              Soumita
            </span> 👻
          </h1>
        </div>

        <!-- Description -->
        <p class="text-gray-300 pt-6 text-center lg:text-left max-w-xl mx-auto lg:mx-0">
          I’m a passionate web developer building elegant and responsive web applications using Vue.js and Tailwind CSS. Let's build something amazing together!
        </p>

        <!-- Download Button -->
        <div class="pt-8 flex justify-center lg:justify-start">
          <a href="/resume.pdf" download="resume.pdf"
            class="flex items-center gap-2 border border-[var(--color-primary)] px-6 py-3 rounded-full text-[var(--color-primary)] hover:scale-105 transition-transform duration-200 ease-in-out">
            <svg width="18" height="22" viewBox="0 0 18 22" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M13 9L9 13M9 13L5 9M9 13V1" stroke="#f59e0b" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
              <path d="M1 17V18C1 18.8 1.3 19.6 1.9 20.1C2.4 20.7 3.2 21 4 21H14C14.8 21 15.6 20.7 16.1 20.1C16.7 19.6 17 18.8 17 18V17"
                stroke="#f59e0b" stroke-width="2" stroke-linecap="round" />
            </svg>
            <span>Download Resume</span>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import AOS from 'aos'
import 'aos/dist/aos.css'

export default {
  mounted() {
    AOS.init({ duration: 1000, once: true })
  }
}
</script>

<style scoped>
/* Add custom styles here if needed */
</style>
