<template>
  <section id="contact" class="text-white select-none mt-20">
    <h2 class="text-4xl font-bold mb-4 px-4 xl:pl-16">Let's <span class="text-transparent bg-clip-text bg-gradient-to-r from-[var(--color-primary)] to-[var(--color-secondary)]">Connect</span></h2>

    <div class="grid md:grid-cols-2 gap-4 relative px-4 xl:px-16 mt-8" data-aos="zoom-in-up">
      
      <!-- Left: Info -->
      <div>
        <p class="text-[#adb7be]">
          I’m always open to new opportunities, collaborations, or just a friendly chat! Whether you have a question, want to discuss a project, or simply want to connect, feel free to drop a message. I’ll try my best to get back to you as soon as possible. Let’s build something awesome together! 
        </p>

        <div class="mt-5 grid grid-cols-1 sm:grid-cols-2 gap-x-6 gap-y-10 py-10">
            <div v-for="(item, index) in contacts" :key="index" class="flex items-center">
              <!-- <a :href="item.url"> -->
                <a class="Logo" v-if="item.url" :href="item.url" target="_blank">
                  <img :src="item.icon" alt="" class="w-6" />
                </a>
                <div v-else class="Logo">
                  <img :src="item.icon" alt="" class="w-6" />
                </div>
                <div class="ml-5">
                    <h4 class="capitalize">{{ item.label }}</h4>
                    <p>{{ item.value }}</p>
                </div>
              <!-- </a> -->
            </div>
        </div>

      </div>

      <!-- Right: Form -->
        <div class="bg-[#101838] w-full h-full rounded-2xl border border-none backdrop-blur-lg p-6">
        <form action="https://api.web3forms.com/submit" class="space-y-6" data-aos="zoom-in-up" method="POST">
          <input type="hidden" name="access_key" value="7e08481c-67df-46e7-ac69-8965dfe1c014">
            <div>
            <label for="email" class="block mb-2 text-sm font-medium text-white">Email</label>
            <div class="focus-within:border-transparent focus-within:bg-gradient-to-r focus-within:from-[var(--color-primary)] focus-within:to-[var(--color-secondary)] p-[2px] rounded-lg transition">
              <input
                type="email"
                id="email" name="email"
                placeholder="Enter your email"
                class="w-full p-3 rounded-lg bg-[#111827] text-white placeholder-gray-400 border border-transparent focus:outline-none"
                required
              />
            </div>
            </div>

            <div>
            <label for="subject" class="block mb-2 text-sm font-medium text-white">Subject</label>
            <div class="focus-within:border-transparent focus-within:bg-gradient-to-r focus-within:from-[var(--color-primary)] focus-within:to-[var(--color-secondary)] p-[2px] rounded-lg transition">
              <input
                  type="text"
                  id="subject" name="submit"
                  placeholder="Subject of your message"
                  class="w-full p-3 rounded-lg bg-[#111827] text-white placeholder-gray-400 border border-gray-600 focus:outline-none transition" required
              />
            </div>
            </div>

            <div>
            <label for="message" class="block mb-2 text-sm font-medium text-white">Message</label>
            <div class="focus-within:border-transparent focus-within:bg-gradient-to-r focus-within:from-[var(--color-primary)] focus-within:to-[var(--color-secondary)] p-[2px] rounded-lg transition">
              <textarea
                  id="message"
                  rows="5" name="message"
                  placeholder="Your message..."
                  class="w-full p-3 rounded-lg bg-[#111827] text-white placeholder-gray-400 border border-gray-600 focus:outline-none transition" required
              ></textarea>
            </div>
            </div>

            <button
            type="submit"
            class="w-full px-6 py-3 rounded-full bg-gradient-to-r from-[var(--color-primary)] to-[var(--color-secondary)] text-white text-[1.1rem] hover:cursor-pointer font-bold hover:bg-opacity-90 transition border-2 border-transparent"
            >
            Send Message
            </button>
        </form>
        </div>
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
          icon: "https://img.icons8.com/metro/50/ffffff/new-post.png",
          url:"",
        },
        {
          label: "linkedin",
          value: "Soumita-Nag",
          icon: "https://img.icons8.com/ios-filled/50/ffffff/linkedin.png",
          url:"https://www.linkedin.com/in/soumita-nag-a3b529314/",
        },
        {
          label: "github",
          value: "Soumita-Nag",
          icon: "https://img.icons8.com/ios-filled/50/ffffff/github.png",
          url:"https://github.com/Soumita-Nag",
        },
        // {
        //   label: "Twitter",
        //   value: "nagsoumita04",
        //   icon: "https://img.icons8.com/ios-filled/50/ffffff/twitter.png",
        //   url:"https://x.com/nagsoumita04",
        // },
        // {
        //   label: "Instagram",
        //   value: "Soumita-Nag",
        //   icon: "https://img.icons8.com/ios-filled/50/ffffff/instagram.png",
        //   url:"",
        // },
        {
          label: "Hackerrank",
          value: "nagsoumita04",
          icon: "https://img.icons8.com/external-tal-revivo-color-tal-revivo/48/external-hackerrank-is-a-technology-company-that-focuses-on-competitive-programming-logo-color-tal-revivo.png",
          url:"https://www.hackerrank.com/profile/nagsoumita04",
        },
        {
          label: "LeetCode",
          value: "Soumita_Nag",
          icon: "https://upload.wikimedia.org/wikipedia/commons/1/19/LeetCode_logo_black.png",
          url:"https://leetcode.com/u/Soumita_Nag",
        },
        {
          label: "GeeksForGeeks",
          value: "nagsoum3bg1",
          icon: "https://upload.wikimedia.org/wikipedia/commons/4/43/GeeksforGeeks.svg",
          url:"https://www.geeksforgeeks.org/user/nagsoum3bg1/",
        },
      ]
    };
  }
};
</script>

<style scoped>
.Logo {
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
