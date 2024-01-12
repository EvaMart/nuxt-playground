<template>
    <div>
      <v-card-subtitle>Number of citations per year</v-card-subtitle>

      <h5 class="ml-5 mb-4 text-subtitle">Simple:</h5>
      <citationsPlot :dataTraces="dataTraces" :showlegend="true" :colors="colors" :width="width"/>

      <h5 class="ml-5 mb-4 text-subtitle">Stacked:</h5>
      <citationsPlot :dataTraces="dataTraces" :showlegend="true" :colors="colors" :stack="true" :width="width"/>

      <h5 class="ml-5 mb-4 text-subtitle">Stacked-dark:</h5>
      <citationsPlot :dataTraces="dataTraces" :showlegend="true" :colors="colors" :stack="true" :darkMode="true" :width="width" />    
   
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
      width: window.width*0.75,
    }
  }
}
</script>
