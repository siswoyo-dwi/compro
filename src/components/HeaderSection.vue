<template>
  <nav class="fixed w-full z-10 bg-gray-900 shadow">
    <div class="container mx-auto px-4">
      <div class="flex justify-between items-center py-4">
        <div class="flex items-center">
          <a class="text-2xl font-bold text-white" href="#">MIB</a>
        </div>
        <div class="hidden md:flex space-x-4">
          <router-link
            v-for="item in navItems"
            :key="item.text"
            :to="item.link"
            class="text-gray-300 hover:bg-gray-800 hover:text-white px-4 py-2 rounded transition duration-300"
          >
            {{ item.text }}
          </router-link>
        </div>
        <div class="md:hidden">
          <button @click="toggleMenu" class="text-white focus:outline-none">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              class="h-6 w-6"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
            </svg>
          </button>
        </div>
      </div>
    </div>

    <!-- Mobile Menu -->
    <transition name="fade">
      <div v-if="isMenuOpen" class="md:hidden">
        <div class="bg-gray-800 space-y-2 py-4">
          <router-link
            v-for="item in navItems"
            :key="item.text"
            :to="item.link"
            class="block px-4 py-2 text-gray-300 hover:bg-gray-700 hover:text-white rounded transition duration-300"
            @click="toggleMenu"
          >
            {{ item.text }}
          </router-link>
        </div>
      </div>
    </transition>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      isMenuOpen: false,
      navItems: [
        { text: "Home", link: "/" },
        { text: "About", link: "/about" },
        { text: "Services", link: "/services" },
        { text: "Guards", link: "/guards" },
        { text: "Contact", link: "/contact" },
      ],
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
  },
};
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
