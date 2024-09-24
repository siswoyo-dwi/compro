<template>
  <div class="surface-0 overflow-hidden" style="min-height: 100vh;">
  <!-- <div class="overflow-hidden py-4"> -->
    <!-- <div class="py-3 relative my-3" style="min-height: 100vh;" id="hero"> -->
        <!-- Navbar Section -->
    <nav class="navbar">
        <div class="navbar-container">
            <a href="#" class="brand-logo">CV MIB LABS</a>
            <button class="navbar-toggle" id="navbarToggle">
                ☰
            </button>
            <ul class="navbar-menu" id="navbarMenu">
                <li><a href="#hero">Home</a></li>
                <li><a href="#about">About Us</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#portfolio">Portfolio</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>
    <Hero/>
    <About/>
    <Services/>
    <Portfolio :graduates="graduates" :projects="projects"/>
    <Contact/>

    <div class="grid mb-6">
      <!-- {{data}} -->
      <div class="md:col-2"></div>
   
      <div class="md:col-2"></div>
      
    </div>
  </div>
</template>

<script>

import  Hero  from "./Hero.vue";
import  About  from "./About.vue";
import  Services  from "./Services.vue";
import  Portfolio  from "./Portfolio.vue";
import  Contact  from "./Contact.vue";
export default {
    components: {
        Hero,
        About,
        Services,
        Portfolio,
        Contact,
  },
  setup () {
  },
  data(){
    return {
        currentIndex: 0,
        autoSlideInterval: null,
      graduates: [
        { name: 'Andi Prasetyo', skills: 'JavaScript, Node.js', year: 2023, project: 'Aplikasi E-commerce', linkedin: '#' },
        { name: 'Siti Nurhaliza', skills: 'PHP, Laravel', year: 2022, project: 'Sistem Manajemen Inventaris', linkedin: '#' },
        { name: 'Andi Prasetyo', skills: 'JavaScript, Node.js', year: 2023, project: 'Aplikasi E-commerce', linkedin: '#' },
        { name: 'Siti Nurhaliza', skills: 'PHP, Laravel', year: 2022, project: 'Sistem Manajemen Inventaris', linkedin: '#' },
        { name: 'Andi Prasetyo', skills: 'JavaScript, Node.js', year: 2023, project: 'Aplikasi E-commerce', linkedin: '#' },
        { name: 'Siti Nurhaliza', skills: 'PHP, Laravel', year: 2022, project: 'Sistem Manajemen Inventaris', linkedin: '#' },
       
        // Add more graduates here
      ],
      projects: [
        { title: 'Aplikasi E-commerce', description: 'Platform belanja online dengan fitur keranjang dan pembayaran.', technology: 'Node.js, MongoDB', year: 2023, github: '#' },
        { title: 'Sistem Manajemen Inventaris', description: 'Aplikasi untuk memonitor stok barang dan laporan penjualan.', technology: 'PHP, MySQL', year: 2022, github: '#' },
        { title: 'Aplikasi E-commerce', description: 'Platform belanja online dengan fitur keranjang dan pembayaran.', technology: 'Node.js, MongoDB', year: 2023, github: '#' },
        { title: 'Sistem Manajemen Inventaris', description: 'Aplikasi untuk memonitor stok barang dan laporan penjualan.', technology: 'PHP, MySQL', year: 2022, github: '#' },
        { title: 'Aplikasi E-commerce', description: 'Platform belanja online dengan fitur keranjang dan pembayaran.', technology: 'Node.js, MongoDB', year: 2023, github: '#' },
        { title: 'Sistem Manajemen Inventaris', description: 'Aplikasi untuk memonitor stok barang dan laporan penjualan.', technology: 'PHP, MySQL', year: 2022, github: '#' },
        { title: 'Aplikasi E-commerce', description: 'Platform belanja online dengan fitur keranjang dan pembayaran.', technology: 'Node.js, MongoDB', year: 2023, github: '#' },
        { title: 'Sistem Manajemen Inventaris', description: 'Aplikasi untuk memonitor stok barang dan laporan penjualan.', technology: 'PHP, MySQL', year: 2022, github: '#' },
        
        // Add more projects here
      ]
    }
  },
  computed: {
  },
  validations () {
    return {
    }
  },
  async mounted() {
    
  },

  methods: {

  },
}
</script>

<style>
/* General Styles */
body {
    font-family: 'Roboto', sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
}

.section {
    padding: 80px 20px;
    text-align: center;
}

</style>