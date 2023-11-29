<template>
    <div>
        <v-card-subtitle>Access time and status of a service accross time </v-card-subtitle>
          <h5 class="ml-5 mb-4 text-subtitle">One month:</h5>
            <accessibilityPlot :dataItems="data" />
            <br>
            <h5 class="ml-5 mb-4 text-subtitle">One week:</h5>
            <accessibilityPlot :dataItems="dataWeek" week />
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
    }
  }
}

</script>