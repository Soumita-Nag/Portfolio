<template>
  <section class="flex justify-between items-center p-6 bg-opacity-50 relative z-20">
    <div class="text-white text-3xl font-black">Soumita <span class="text-[var(--color-primary)]">Nag</span></div>
    <div class="md:hidden z-30">
      <button type="button" class="block text-[var(--color-primary)] focus:outline-none" @click="toggleMenu">
        <span v-if="isMenuOpen" class="text-5xl">
          <img src="https://img.icons8.com/ios-filled/100/ffffff/delete-sign.png" alt="close" width="50" height="50" />
        </span>
        <span v-else class="text-5xl">
          <img src="https://img.icons8.com/ios-filled/100/ffffff/menu--v1.png" alt="menu" width="50" height="50" />
        </span>
      </button>
    </div>
    <nav
      :class="[
        'fixed inset-0 z-20 flex flex-col items-center justify-center bg-[var(--color-bg)] md:relative md:bg-transparent md:flex md:justify-between md:flex-row',
        isMenuOpen ? 'block' : 'hidden'
      ]"
    >
      <ul class="flex flex-col items-center space-y-5 md:flex-row md:space-x-5 md:space-y-0">
        <li v-for="item in Menu" :key="item.name">
          <a
            :href="item.href"
            class="block text-white transition hover:text-[var(--color-primary)] ease-linear text-2xl md:text-lg"
            @click.prevent="scrollToSection(item.href)"
          >
            {{ item.name }}
          </a>
        </li>
      </ul>
    </nav>
  </section>
</template>

<script>
export default {
  data() {
    return {
      isMenuOpen: false,
      Menu: [
        { name: 'Home', href: '#home' },
        { name: 'About', href: '#about' },
        { name: 'Skills', href: '#skills' },
        { name: 'Projects', href: '#projects' },
        { name: 'Achievements', href: '#achievements' },
        { name: 'Contact', href: '#contact' }
      ]
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
    scrollToSection(href) {
      this.isMenuOpen = false;
      const section = document.querySelector(href);
      if (section) {
        section.scrollIntoView({ behavior: 'smooth' });
      }
    }
  }
};
</script>

<style scoped>
</style>
