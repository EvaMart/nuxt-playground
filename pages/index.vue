<template>
  <v-container fluid>
    <v-row justify="center" align="center">
      <v-col cols="12" sm="10" md="10">
        <h1 class="mb-3">OEB charts demo</h1>
        <v-alert
          dark
          dense
          border="left"
          class="text-caption"
          >

          👷🏻 OEB charts is in development. New components will be progressively added and all components are subjected to changes.
          </v-alert>
        
      </v-col>
    </v-row>
    <v-row justify="center" align="center">
      <v-col cols="12" sm="10" md="10">
        <h2>Components</h2>
        <v-card class="pl-8 pr-8 pb-4 mt-4">
          <v-card-title>Uptime</v-card-title>
          <v-card-subtitle>Access time and status of a service accross time </v-card-subtitle>
          <v-card-content>
            <accessibilityPlot />
            <p class="mt-4 text-body-2">
              Built using <a href="https://plotly.com/javascript/" target="_black">plotly.js</a>
            </p>
        
          </v-card-content>
        </v-card>
      </v-col>
    </v-row>
    
</v-container>
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
