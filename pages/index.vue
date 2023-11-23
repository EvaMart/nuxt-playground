<template>
  <v-container fluid>
    <v-row justify="center" align="center">
      <v-col cols="12" sm="10" md="10">
        <h1 class="mb-3">OEB Visualizations Demo</h1>
        <v-alert
          dark
          dense
          border="left"
          class="text-caption"
          >

          👷🏻 OEB Visualizations is in development. New components will be progressively added and all components are subjected to changes.
          </v-alert>
        
      </v-col>
    </v-row>
    <v-row justify="center" align="center">
      <v-col cols="12" sm="10" md="10">
        <h2>Components</h2>
      </v-col>
      <v-col cols="12" sm="10" md="10">
        <v-card class="pl-8 pr-8 pb-4 mt-4">
          <v-card-title>accessibilityPlot</v-card-title>
          <accessibilityPlotPage />
        </v-card>
      </v-col>
      <v-col cols="12" sm="10" md="10">
        <v-card class="pl-8 pr-8 pb-4 mt-4">
        <v-card-title>citationsPlot</v-card-title>
          <citationsPlotPage />
        </v-card>
      </v-col>
    </v-row>
    
</v-container>
</template>

<script>
import accessibilityPlotPage from '../components/accessibilityPlotPage.vue'
import citationsPlotPage from '../components/citationsPlotPage.vue'
import { data } from '../data/uptime30days.js'



export default {
  name: 'IndexPage',
  components: {
    accessibilityPlotPage,
    citationsPlotPage
  },
  data(){
    return {
      data: data,
    }
  }
}
</script>
