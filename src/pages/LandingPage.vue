<template>
  <div>
    <HeaderSection />
    <HeroSection />
    <AboutSection />
    <ServicesSection />
    <TestimonialsSection />
    <ContactSection />
    <FooterSection />
  </div>
</template>

<script>
import HeaderSection from '../components/HeaderSection.vue';
import HeroSection from '../components/HeroSection.vue';
import AboutSection from '../components/AboutSection.vue';
import ServicesSection from '../components/ServicesSection.vue';
import TestimonialsSection from '../components/TestimonialsSection.vue';
import ContactSection from '../components/ContactSection.vue';
import FooterSection from '../components/FooterSection.vue';

export default {
  components: {
    HeaderSection,
    HeroSection,
    AboutSection,
    ServicesSection,
    TestimonialsSection,
    ContactSection,
    FooterSection,
  },
};
</script>

<style>
/* Global styles can be added here */
</style>
