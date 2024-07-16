<template>
  <v-layout class="rounded rounded-md">
    <v-app-bar scroll-behavior="hide" flat class="px-8 opacity-90">
      <v-app-bar-title data-aos="fade-down">
        <NuxtLink to="/" style="text-decoration: none;"><span class="text-h6 title">A63 Studios</span></NuxtLink>
      </v-app-bar-title>
      <template v-slot:append>
        <NuxtLink to="/services">
          <v-btn variant="text" data-aos="fade-down">Services</v-btn>
        </NuxtLink>
        <NuxtLink to="/about">
          <v-btn variant="text" data-aos="fade-down">About</v-btn>
        </NuxtLink>
        <NuxtLink to="/contact">
          <v-btn variant="flat" color="#fafafa" data-aos="fade-down">Start a Project</v-btn>
        </NuxtLink>
      </template>
    </v-app-bar>

    <v-main class="d-flex align-center justify-center" style="min-height: 300px;">
      <slot />
    </v-main>

    <!-- <AppHeader />

    <AppFooter /> -->
  </v-layout>
</template>

<script setup>
import AOS from 'aos';
import 'aos/dist/aos.css';
import { onMounted } from 'vue';

onMounted(() => {
  AOS.init();
})
</script>