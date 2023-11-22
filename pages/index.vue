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
        <v-card class="pl-8 pr-8 pb-4 mt-4">
          <v-card-title>accessibilityPlot</v-card-title>
          <v-card-subtitle>Access time and status of a service accross time </v-card-subtitle>
          
            <accessibilityPlot :dataItems="data" />
          
        </v-card>
      </v-col>
    </v-row>
    
</v-container>
</template>

<script>
import { accessibilityPlot } from '@inb/oeb_visualizations'
//import { accessibilityPlot } from 'oeb_visualizations'
import { data } from '../data/uptime30days.js'


export default {
  name: 'IndexPage',
  components: {
    accessibilityPlot
  },
  data(){
    return {
      data: data
    }
  }
}
</script>
