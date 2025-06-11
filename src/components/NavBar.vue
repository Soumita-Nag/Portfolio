<template>
  <section class="flex justify-between items-center p-6 relative z-20 bg-opacity-50">
    <div class="text-white text-3xl font-bold">
      Soumita <span class="text-[var(--color-primary)]">Nag</span>
    </div>

    <!-- Mobile menu toggle -->
    <div class="md:hidden z-30">
      <button @click="toggleMenu" class="text-[var(--color-primary)] focus:outline-none">
        <img
          :src="isMenuOpen ? 'https://img.icons8.com/ios-filled/100/ffffff/delete-sign.png' : 'https://img.icons8.com/ios-filled/100/ffffff/menu--v1.png'"
          :alt="isMenuOpen ? 'close' : 'menu'"
          width="30"
          height="30"
        />
      </button>
    </div>

    <!-- Navigation Menu -->
    <nav
      :class="[
        'fixed inset-0 z-20 bg-[var(--color-bg)] md:relative md:bg-transparent md:flex md:items-center md:space-x-6',
        isMenuOpen ? 'flex flex-col justify-center space-y-6' : 'hidden md:flex'
      ]"
    >
      <ul class="flex flex-col items-center md:flex-row md:space-y-0 space-y-6 md:space-x-6">
        <li v-for="item in Menu" :key="item.name">
          <a
            :href="item.href"
            class="text-white text-xl md:text-base hover:text-[var(--color-primary)] transition"
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
      if (section) section.scrollIntoView({ behavior: 'smooth' });
    }
  }
};
</script>

<style scoped>
</style>
