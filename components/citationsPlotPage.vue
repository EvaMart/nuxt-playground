<template>
    <div>
        <v-tabs
        v-model="tabCitations"
        active-class="white--text"
        centered
        dark
        >
        <v-tabs-slider color="white"></v-tabs-slider>
        <v-tab>
            Simple
        </v-tab>
        <v-tab>
            Stacked
        </v-tab>
        <v-tab>
            Stacked - dark
        </v-tab>
        </v-tabs>
          
        <v-tabs-items v-model="tabCitations">
        <v-tab-item>
            <v-card-subtitle>Number of citations per year</v-card-subtitle>
            <citationsPlot :dataTraces="dataTraces" :showlegend="true" :colors="colors" :width="width"/>
        </v-tab-item>
        <v-tab-item>
            <v-card-subtitle>Number of citations per year (stack)</v-card-subtitle>
            <citationsPlot :dataTraces="dataTraces" :showlegend="true" :colors="colors" :stack="true" :width="width"/>
        </v-tab-item>
        <v-tab-item>
            <v-card-subtitle>Number of citations per year (stack)</v-card-subtitle>
            <citationsPlot :dataTraces="dataTraces" :showlegend="true" :colors="colors" :stack="true" :darkMode="true" :width="width" />
        </v-tab-item>
        </v-tabs-items>
    </div>
</template>
<script>
import { citationsPlot } from '@inb/oeb_visualizations'

import { mockData1, mockData2, mockData3 } from '../data/citations10years.js';

export default {
  name: 'citationsPlotPage',
  components: {
    citationsPlot
  },
  data(){
    return {
      dataTraces: [mockData1, mockData2, mockData3],
      colors: ['#004c6d','#6b93b1','#c3e1fa'],
      tabCitations: 0,
      width: window.width*0.8,
    }
  }
}
</script>
