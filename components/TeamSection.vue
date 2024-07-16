<template>
  <v-container class="pa-6 pa-md-12">
    <v-row class="mb-12" justify="center" data-aos="fade-down">
      <v-col cols="12" lg="8" md="12">
        <p class="text-h5 font-weight-bold text-sm-h4 text-center text-primary">
          Our Mission
        </p>
        <p>
          At A63 Studios, our mission is to empower businesses by creating unique websites that are not only visually
          stunning but also highly functional and user-friendly. We believe that a strong online presence is crucial for
          success in today's digital world.<strong class="text-primary"> Making the internet a more beautiful
            place, one
            website
            at a time.</strong>
        </p>
      </v-col>
    </v-row>
    <v-row class="my-8" justify="center" data-aos="zoom-out">
      <v-col cols="12" lg="8" md="12">
        <p class="text-h5 font-weight-bold text-sm-h4 text-center text-primary">
          Why Choose Us?
        </p>
        <v-list-item v-for="(item, i) in features" :key="i" class="px-0">
          <template #title>
            <p class="text-body-2 font-weight-bold pb-2">
              <v-icon class="mr-2" color="primary" :icon="item.icon" size="small" />
              {{ item.title }}
            </p>
          </template>

          <template #subtitle>
            <p class="ps-7">{{ item.subtitle }}</p>
          </template>
        </v-list-item>
      </v-col>
    </v-row>
    <v-row class="my-8" justify="center" data-aos="fade-up">
      <v-col cols="12" lg="8" md="12">
        <p class="text-h5 font-weight-bold text-sm-h4 text-center text-primary">
          About A63 Studios
        </p>

        <p class="mt-4 text-body-1 text-medium-emphasis">
          With over half a decade of web development experience, our team is equipped to deliver high-quality websites
          tailored to your needs. We bring a wealth of knowledge from diverse industries, including the Internet of
          Things (IoT), financial services, and education. This broad experience has equipped us with invaluable
          skills
          and best practices, ensuring we can tackle any challenge and deliver exceptional results.
        </p>
      </v-col>
    </v-row>
    <v-row class="my-8" justify="center" data-aos="flip-down">
      <v-col cols="12" lg="8" md="12">
        <p class="text-h5 font-weight-bold text-sm-h4 text-center text-primary">
          Our Process
        </p>
        <v-list-item v-for="(item, i) in processes" :key="i" class="px-0">
          <template #title>
            <p class="text-body-2 font-weight-bold pb-2">
              <v-icon class="mr-2" color="primary" :icon="item.icon" />

              {{ item.title }}
            </p>
          </template>

          <template #subtitle>
            <p class="ps-7">{{ item.subtitle }}</p>
          </template>
        </v-list-item>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
const items = [
  {
    title: 'Steve Martin',
    subtitle: 'Founder / CEO',
    avatar: 'https://vuetifyjs.b-cdn.net/images/john-smirk.png',
  },
]

const features = [
  {
    title: 'Over Half a decade of experience',
    subtitle:
      "More than half a decabe of experience across various sectors, we've learned a thing or two about successful sites.",
    icon: 'mdi-calendar-outline',

  },
  {
    title: 'Not another cookie cutter website provider',
    subtitle:
      'We understand that your website is an extension of your brand and identity. We believe a fully bespoke experience enables you to showcase your uniqness.',
    icon: 'mdi-cookie-off',
  },
  {
    title: 'Hassle-free Development',
    subtitle:
      'We streamline every step of the development process to ensure a smooth and hassle-free experience. From initial consultation to final launch, we handle all the details so you can focus on your business.',
    icon: 'mdi-cogs',
  },
  {
    title: 'Client Satisfaction',
    subtitle:
      'Our clients are at the heart of everything we do, and their satisfaction is our top priority.',
    icon: 'mdi-account-multiple',
  },
]

const processes = [
  {
    title: 'Discovery',
    subtitle:
      "We start by understanding your business, goals, and target audience.",
    icon: 'mdi-numeric-1',
  },
  {
    title: 'Planning',
    subtitle:
      "We create a detailed project plan and timeline to ensure smooth execution.",
    icon: 'mdi-numeric-2',
  },
  {
    title: 'Design',
    subtitle:
      "Our designers craft visually appealing and user-friendly designs.",
    icon: 'mdi-numeric-3',
  },
  {
    title: 'Development',
    subtitle:
      "Our developers bring the designs to life with clean, efficient code.",
    icon: 'mdi-numeric-4',
  },
  {
    title: 'Testing',
    subtitle:
      "We rigorously test the website to ensure it functions flawlessly.",
    icon: 'mdi-numeric-5',
  },
  {
    title: 'Launch',
    subtitle:
      "We launch the website and provide ongoing support and maintenance.",
    icon: 'mdi-numeric-6',
  },
]
</script>