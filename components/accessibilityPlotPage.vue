<template>
    <div>
        <v-card-subtitle>Access time and status of a service accross time </v-card-subtitle>
            <accessibilityPlot :dataItems="data" />
    </div>
</template>
<script>
import { accessibilityPlot } from '@inb/oeb_visualizations'
import { data } from '../data/uptime30days.js'

export default {
  name: 'accessibilityPlotPage',
  components: {
    accessibilityPlot
  },
  data(){
    return {
      data: data,
    }
  }
}

</script>