<template>
  <section class="text-white mt-10 select-none">  
    <!-- Main Grid Layout -->
    <div class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-8 sm:py-16 xl:px-16 relative z-10">
    <!-- Education Section -->
        <div data-aos="flip-right">
        <h2 class="text-4xl font-bold text-left mb-8">My <span class="text-transparent bg-clip-text bg-gradient-to-r from-[var(--color-primary)] to-[var(--color-secondary)]">Education</span></h2>
        <div class="space-y-5 py-8">
            <div
            v-for="e in education"
            :key="e.id"
            class="flex items-center hover:scale-105 hover:bg-[#152049] cursor-pointer w-full md:w-[80%] bg-[#111a3e]/80 border border-[#1f1641] rounded-2xl shadow-lg hover:shadow-2xl transition duration-300 p-4 backdrop-blur-md"
            >
            <!-- Image with ring effect -->
            <div class="w-1/4 flex justify-center items-center">
                <div class="p-2 rounded-full bg-gradient-to-br from-[var(--color-primary)] to-[var(--color-secondary)]">
                <img
                    class="w-14 h-14 p-1 bg-[#111a3e] rounded-full"
                    src="https://img.icons8.com/ios-glyphs/60/ffffff/graduation-cap--v1.png"
                    alt="graduation cap"
                />
                </div>
            </div>

            <!-- Text Section -->
            <div class="w-[100%] pl-6">
                <h3 class="text-[1.15rem] font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-[var(--color-primary)] to-[var(--color-secondary)]">
                {{ e.program }}
                </h3>
                <p class="text-[1rem] text-white mt-1">{{ e.school }}</p>
                <div class="flex justify-between"> 
                  <p class="text-sm text-gray-400" v-if="e.id==1 || e.id==2">CGPA : {{ e.grade }}</p>
                  <p class="text-sm text-gray-400" v-else>Percentage : {{ e.grade }}</p>
                  <p class="text-[0.8rem] text-gray-400">{{ e.yearFrom }} - {{ e.yearTo }}</p>
                </div>
            </div>
            </div>  
        </div>
        </div>
      <!-- About Me Section -->
      <div class="mt-4 md:mt-0 flex flex-col h-full" data-aos="flip-right">
        <h2 class="text-4xl font-bold mb-4 md:text-center">
          More
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-[var(--color-primary)] to-[var(--color-secondary)]">About</span>
          Me
        </h2>
        <p class="text-base lg:text-lg mt-8 py-8">
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Hi, I'm Soumita Nag, a dedicated and creative web developer with a strong passion for building visually stunning and highly functional web applications. I strive to craft seamless, responsive, and user-friendly digital experiences. I love turning ideas into interactive realities. Beyond code, I'm also an active learner in Data Structures, Algorithms, and emerging tech trends. <br>
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Currently pursuing my MCA at Jadavpur University, I’ve been actively involved in various projects, from personal passion apps to collaborative team efforts, where I’ve honed my skills in frontend development, problem-solving, and clean UI/UX design. I also take pride in participating in coding challenges and contributing to open-source events like GirlScript Summer of Code and Ninja Slayground. <br>
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Beyond the code, I’m a martial artist, self-defense student, and a firm believer in discipline and focus—qualities I carry into my development workflow. I’m always looking for new challenges, exciting projects, and meaningful collaborations that push the boundaries of what I can create on the web.
        </p>
      </div>
      <div id="skills"></div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AboutSection',
  data() {
    return {
      education: [
        {
          id: 1,
          school: 'Jadavpur University',
          program: 'Master of Computer Application (MCA)',
          yearFrom: 2024,
          yearTo: 'Present',
          grade: 'Not Available'
        },
        {
          id: 2,
          school: 'Banwarilal Bhalotia College, Asansole',
          program: 'BSc. in Computer Science',
          yearFrom: 2021,
          yearTo: 2024,
          grade: '8.84'
        },
        {
          id: 3,
          school: 'Gandhi Memorial Girls High School(HS), Raniganj',
          program: 'Higher Secondary (WBCHSE)',
          yearFrom: 2020,
          yearTo: 2021,
          grade: '87.6'
        },
        {
          id: 4,
          school: 'Gandhi Memorial Girls High School(HS), Raniganj',
          program: 'Secondary (WBSE)',
          yearFrom: 2018,
          yearTo: 2019,
          grade: '85.57'
        }
      ]
    };
  }
};
</script>

<style scoped>
</style>
