<template>
  <div class="d-flex flex-column w-100">
    <section id="hero" class="d-flex w-100 align-center" style="background: #fafafa; height: 100vh">
      <HeroSection></HeroSection>
    </section>
    <section id="work" data-aos="fade-up" class="d-flex w-100">
      <FeaturesSection></FeaturesSection>
    </section>
    <section id="services" class="d-flex w-100" style="background: #fafafa;" data-aos="fade-left">
      <ServicesSection></ServicesSection>
    </section>
    <section id="about" data-aos="fade-right">
      <AboutSection></AboutSection>
    </section>
    <section id="testimonials" data-aos="fade-up" style="background: #fafafa;">
      <TestimonialSection></TestimonialSection>
    </section>
    <section id="clients" data-aos="fade-up">
      <ClientsSection></ClientsSection>
    </section>
    <section id="action" class="d-flex w-100" style="background: #fafafa;" data-aos="fade-up">
      <ActionSection></ActionSection>
    </section>
  </div>
</template>

<script setup>
import AOS from 'aos';
import 'aos/dist/aos.css';
import { onMounted } from 'vue';

onMounted(() => {
  AOS.init();
})
</script>