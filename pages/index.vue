<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <v-card class="logo py-4 d-flex justify-center">
      </v-card>
      <v-card>
        Nuxt Playground 🫶🏻
        <accessibilityPlot />
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
import { accessibilityPlot } from 'oeb_visualizations'

export default {
  name: 'IndexPage',
  components: {
    accessibilityPlot
  }
}
</script>
