<template>
  <section id="contact" class="text-white mt-20">
    <h2 class="text-4xl font-bold mb-4 px-4 xl:pl-16">Let's <span class="text-transparent bg-clip-text bg-gradient-to-r from-[var(--color-primary)] to-[var(--color-secondary)]">Connect</span></h2>

    <div class="grid md:grid-cols-2 gap-4 relative px-4 xl:px-16 mt-8" data-aos="zoom-in-up">
      
      <!-- Left: Info -->
      <div>
        <p class="text-[#adb7be]">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed optio repudiandae porro quia? Pariatur dolores totam debitis, architecto ipsam repellat voluptatum neque aliquid, laboriosam corrupti temporibus tempora sit quaerat atque, facilis reprehenderit asperiores earum?
        </p>

        <div class="mt-5 grid grid-cols-1 sm:grid-cols-2 gap-x-6 gap-y-10">
            <div v-for="(item, index) in contacts" :key="index" class="flex items-center">
                <div class="emailLogo">
                    <img :src="item.icon" alt="" class="w-6" />
                </div>
                <div class="ml-5">
                    <h4 class="capitalize">{{ item.label }}</h4>
                    <p>{{ item.value }}</p>
                </div>
            </div>
        </div>

      </div>

      <!-- Right: Form -->
        <div class="bg-[#111a3e] w-full h-full rounded-2xl border border-[#111a3e] backdrop-blur-lg p-6">
        <form class="space-y-6" data-aos="zoom-in-up">
            <div>
            <label for="email" class="block mb-2 text-sm font-medium text-white">Email</label>
            <input
                type="email"
                id="email"
                placeholder="Enter your email"
                class="w-full p-3 rounded-lg bg-[#111827] text-white placeholder-gray-400 border border-gray-600 focus:outline-none focus:ring-2 focus:ring-[var(--color-primary)] transition"
            />
            </div>

            <div>
            <label for="subject" class="block mb-2 text-sm font-medium text-white">Subject</label>
            <input
                type="text"
                id="subject"
                placeholder="Subject of your message"
                class="w-full p-3 rounded-lg bg-[#111827] text-white placeholder-gray-400 border border-gray-600 focus:outline-none focus:ring-2 focus:ring-[var(--color-primary)] transition"
            />
            </div>

            <div>
            <label for="message" class="block mb-2 text-sm font-medium text-white">Message</label>
            <textarea
                id="message"
                rows="5"
                placeholder="Your message..."
                class="w-full p-3 rounded-lg bg-[#111827] text-white placeholder-gray-400 border border-gray-600 focus:outline-none focus:ring-2 focus:ring-[var(--color-primary)] transition"
            ></textarea>
            </div>

            <button
            type="submit"
            class="w-full px-6 py-3 rounded-full bg-[var(--color-primary)] text-white font-semibold hover:bg-opacity-90 transition border-2 border-transparent"
            >
            Send Message
            </button>
        </form>
        </div>


      <!-- Background Glow -->
      <div class="bg-gradient-to-tr opacity-25 from-[#570cac] to-[var(--color-primary)] blur-2xl h-20 w-80 z-0 absolute -top-1/2 -left-4 -translate-x-2/3 -translate-y-1/2"></div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      contacts: [
        {
          label: "email",
          value: "nagsoumita04@gmail.com",
          icon: "https://img.icons8.com/metro/50/ffffff/new-post.png"
        },
        {
          label: "linkedin",
          value: "Soumita-Nag",
          icon: "https://img.icons8.com/ios-filled/50/ffffff/linkedin.png"
        },
        {
          label: "github",
          value: "Soumita-Nag",
          icon: "https://img.icons8.com/ios-filled/50/ffffff/github.png"
        },
        {
          label: "Twitter",
          value: "Soumita-Nag",
          icon: "https://img.icons8.com/ios-filled/50/ffffff/twitter.png"
        },
        {
          label: "Instagram",
          value: "Soumita-Nag",
          icon: "https://img.icons8.com/ios-filled/50/ffffff/instagram.png"
        },
        {
          label: "Hackerrank",
          value: "Soumita-Nag",
          icon: "https://img.icons8.com/external-tal-revivo-color-tal-revivo/48/external-hackerrank-is-a-technology-company-that-focuses-on-competitive-programming-logo-color-tal-revivo.png"
        },
        {
          label: "LeetCode",
          value: "Soumita-Nag",
          icon: "https://upload.wikimedia.org/wikipedia/commons/1/19/LeetCode_logo_black.png"
        },
        {
          label: "GeeksForGeeks",
          value: "Soumita-Nag",
          icon: "https://upload.wikimedia.org/wikipedia/commons/4/43/GeeksforGeeks.svg"
        },
      ]
    };
  }
};
</script>

<style scoped>
.emailLogo {
  background: #111a3e;
  width: 50px;
  height: 46px;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
  overflow: hidden;
  border: 1px solid #111a3e;
  backdrop-filter: blur(9px);
  -webkit-backdrop-filter: blur(9px);
}
</style>
