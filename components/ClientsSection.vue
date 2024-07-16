<template>
  <v-container class="text-center pa-md-12 pa-6" fluid>
    <v-row justify="center">
      <Vue3Marquee>
        <v-col v-for="(item, i) in items" :key="i" cols="6" lg="2" md="4" sm="3">
          <v-img class="mx-auto" max-width="160" :src="item" />
        </v-col>
      </Vue3Marquee>
    </v-row>
  </v-container>
</template>

<script setup>
import { useTheme } from 'vuetify';
const theme = useTheme()

const items = computed(() => [
  `https://upload.wikimedia.org/wikipedia/commons/9/95/Vue.js_Logo_2.svg`,
  `https://nuxt.com/assets/design-kit/icon-green.svg`,
  `https://cdn.vuetifyjs.com/docs/images/brand-kit/v-logo-atom.svg`,
  `https://nodejs.org/static/logos/nodejsDark.svg`,
  `https://images.spr.so/cdn-cgi/imagedelivery/j42No7y-dcokJuNgXeA0ig/32f3a89c-99c4-466f-8536-dd75f65fa320/Strapi-Monogram/w=256,quality=90,fit=scale-down.png`,
  `https://upload.wikimedia.org/wikipedia/commons/5/5e/Vercel_logo_black.svg`,
  // `https://vuetifyjs.b-cdn.net/docs/images/one/logos/vstudio-logo-${theme.current.value.dark ? 'dark' : 'light'}.png`,
])
</script>