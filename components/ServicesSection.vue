<template>
  <v-container class="pa-md-12 pa-sm-6" fluid>
    <v-responsive class="text-center mx-auto mb-6 mb-md-12" max-width="700">
      <h1 class="text-md-h4 font-weight-bold mb-4 text-sm-h5" style="color: #0f0f0f !important;">
        Gain access for One Price
      </h1>

      <p class="text-subtitle-1 text-medium-emphasis" style="color: #0f0f0f !important;">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi,
        ratione debitis quis est labore voluptatibus! Eaque cupiditate
        minima, at placeat totam.
      </p>
    </v-responsive>

    <v-sheet border class="mx-auto pa-2" max-width="1000" rounded="xl" color="#fafafa">
      <v-row>
        <v-col cols="12" md="4">
          <v-card border class="h-100 flex-column d-flex align-center justify-center pa-4" color="grey" rounded="xl"
            variant="tonal">
            <div class="text-subtitle-1 font-weight-medium mb-3 opacity-70 text-high-emphasis"
              style="color: #0f0f0f !important;">
              Pay once, get access forever
            </div>

            <div class="text-h3 mb-8 text-black font-weight-bold">
              $199
              <small class="text-overline">USD</small>
            </div>

            <v-btn class="mb-5 text-none" color="success" max-height="36" max-width="256" rounded="lg" text="Get access"
              variant="flat" width="100%" />

            <div class=" w-75" style="color: #0f0f0f;">
              <span class="text-caption text-medium-emphasis text-center" style="color: #0f0f0f !important;"> ipsum
                dolor sit
                amet
                consectetur adipisicing elit. </span>
            </div>
          </v-card>
        </v-col>

        <v-col class="pa-6" cols="12" md="8">
          <h2 class="text-h5 font-weight-bold mb-4">Lifetime subscription</h2>

          <p class="text-medium-emphasis mb-4" style="color: #0f0f0f !important;">
            Get the most out of Vuetify with a lifetime subscription. This
            is a limited time offer and will not be available in the future.
            Get access to all current and future features, including full
            access to all snips components.
          </p>

          <div class="d-flex align-center mb-8">
            <span class="text-primary text-no-wrap text-body-2 font-weight-medium me-4">What you get</span>
            <v-divider />
          </div>
          <v-row dense>
            <v-col v-for="feature in features" :key="feature" cols="12" md="6">
              <v-icon color="success" icon="$success" />
              <span class="text-caption ms-2"> {{ feature }} </span>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-sheet>
  </v-container>
</template>

<script setup>
const features = [
  'Savable Bin and Playgrounds',
  'Full access to all snips components',
  'Access to all current and future features',
  'Lifetime Vuetify One access',
]
</script>