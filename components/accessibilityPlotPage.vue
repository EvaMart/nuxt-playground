<template>
    <div>
        <v-card-subtitle>Access time and status of a service accross time </v-card-subtitle>
          <h5 class="ml-5 mb-4 text-subtitle">One month:</h5>
          <accessibilityPlot :dataItems="data" :width="width"/>
          <br>
          <h5 class="ml-5 mb-4 text-subtitle">One week:</h5>
          <accessibilityPlot :dataItems="dataWeek" :width="width" week />
          <br>

          <h5 class="ml-5 mb-4 text-subtitle">6 months:</h5>
          <accessibilityPlot :dataItems="dataSixMonths" sixMonths :width="width" />
    </div>
</template>
<script>
import { accessibilityPlot } from '@inb/oeb_visualizations'
import { data } from '../data/uptime30days.js'
import { dataWeek } from '../data/uptimeWeek.js'

export default {
  name: 'accessibilityPlotPage',
  components: {
    accessibilityPlot
  },
  data(){
    return {
      data: data,
      dataWeek: dataWeek,
      width: window.width*0.75,
    }
  },
}

</script>