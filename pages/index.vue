<template>
  <v-container fluid>
    <v-row justify="center" align="center">
      <v-col cols="12" sm="10" md="10" class="d-flex justify-space-between">
        <h1>
          OEB Visualizations Demo
        </h1>
        <a class="d-flex github" href="https://github.com/inab/oeb-visualizations/" target="_blank">
          <v-icon class="align-self-center">
           mdi-github
        </v-icon>
        </a>
        

        
      </v-col>
      <v-col cols="12" sm="10" md="10">  
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
          <v-card-title>Scatter Plot</v-card-title>
          <accessibilityPlotPage />
        </v-card>
      </v-col>
    </v-row>
    
</v-container>
</template>

<script>

import scatterPlotPage from '../components/scatterPlotPage.vue'
import { data } from '../data/uptime30days.js'



export default {
  name: 'IndexPage',
  components: {
    scatterPlotPage
  },
  data(){
    return {
      data: data,
    }
  }
}
</script>


<style scoped>

.github{
  text-decoration: none;
}

</style>
