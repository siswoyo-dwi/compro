<template>
  <section class="relative bg-cover bg-center h-screen hero-section" style="background-image: url('images/hero-bg.jpg');">
    <div class="flex items-center justify-center h-full bg-black bg-opacity-50">
      <div class="text-center text-white max-w-xl">
        <h1 class="text-5xl font-bold mb-4 animate__animated animate__fadeInDown">Your Safety</h1>
        <h2 class="text-3xl mb-6 animate__animated animate__fadeInUp">Our Responsibility</h2>
        <p class="mb-8 animate__animated animate__fadeIn">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
        <div class="flex justify-center space-x-4">
          <router-link to="/read-more" class="bg-blue-500 hover:bg-blue-700 text-white font-semibold py-2 px-4 rounded transition duration-300 animate__animated animate__bounceIn">Read More</router-link>
          <router-link to="/get-quote" class="bg-transparent border border-white hover:bg-white hover:text-gray-900 text-white font-semibold py-2 px-4 rounded transition duration-300 animate__animated animate__bounceIn">Get A Quote</router-link>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import 'animate.css';

export default {
  name: "HeroSection",
};
</script>

<style scoped>
.hero-section {
  height: 100vh; /* Full viewport height */
}
</style>
