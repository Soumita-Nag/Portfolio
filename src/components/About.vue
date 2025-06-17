<template>
  <section class="text-white mt-10">
    <!-- Gradient Background -->
    <div class="absolute z-0 top-[93rem] inset-x-0 h-64 flex items-start">
      <div class="h-24 w-64 bg-gradient-to-br from-[var(--color-primary)] via-[var(--color-secondary)] to-[#570cac] blur-2xl opacity-20"></div>
    </div>

    <!-- Main Grid Layout -->
    <div class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-16 sm:py-16 xl:px-16 relative z-10">
    <!-- Education Section -->
        <div data-aos="flip-right">
        <h2 class="text-4xl font-bold text-left mb-8">My <span class="text-transparent bg-clip-text bg-gradient-to-r from-[var(--color-primary)] to-[var(--color-secondary)]">Education</span></h2>
        <div class="space-y-8 py-8">
            <div
            v-for="e in education"
            :key="e.id"
            class="flex items-center w-full md:w-[80%] bg-[#111a3e]/80 border border-[#1f1641] rounded-2xl shadow-lg hover:shadow-2xl transition duration-300 p-4 backdrop-blur-md"
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
            <div class="w-3/4 pl-6">
                <h3 class="text-xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-[var(--color-primary)] to-[var(--color-secondary)]">
                {{ e.school }}
                </h3>
                <p class="text-sm text-white mt-1">{{ e.program }}</p>
                <p class="text-sm text-gray-400">{{ e.yearFrom }} - {{ e.yearTo }}</p>
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
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Et inventore quisquam, maxime mollitia temporibus facere facilis ex dolore porro iure eveniet esse quae, dignissimos molestias pariatur unde assumenda, enim tenetur laudantium accusantium perferendis architecto!
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
          yearTo: 'Present'
        },
        {
          id: 2,
          school: 'Banwarilal Bhalotia College, Asansole',
          program: 'BSc. in Computer Science',
          yearFrom: 2021,
          yearTo: 2024
        }
      ]
    };
  }
};
</script>

<style scoped>
</style>
