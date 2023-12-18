<template>
    <div>
        <!--Plot goes here-->
        <scatterPlot :data="series" :pareto="paretoFront"/>
    </div>

</template>
<script>
// import plot form library
import { scatterPlot } from '@inb/oeb_visualizations'
const pf = require('pareto-frontier');
// import data
import { data } from '../data/OEBD00200002V2-inline.js'

const paretoMappings = {
                "bottom-left": 'bottomLeft',
                "bottom-right": 'bottomRight',
                "top-left": 'topLeft',
                "top-right": 'topRight',
            }

export default {
    name: 'scatterPlotPage',
    components: {
        scatterPlot
    },
    data() {
        return {
            rawData : data,
            series : this.prepareData(data),
            paretoFront: this.computeParetoFront(data),
            
        }
    },
    methods: {
        prepareData(data){
            // ALL THIS IS THE PROCCESING STEP
        
            // each point in challenge_participants is a trace in the plot
            // each trace has a name and a list of x and y values
            let series = []
            for (let i = 0; i < data.challenge_participants.length; i++) {
                let serie = {
                    name: data.challenge_participants[i].tool_id,
                    x: [ data.challenge_participants[i].metric_x ],
                    y: [ data.challenge_participants[i].metric_y ],
                    error_x: {
                        type: 'data',
                        symmetric: true,
                        array: [ data.challenge_participants[i].stderr_x ],                    
                    },
                    error_y: {
                        type: 'data',
                        symmetric: true,
                        array: [ data.challenge_participants[i].stderr_y ],
                    }
                }
                series.push(serie)
                }
            
            
            // this is the data that will be passed to the plot
            return series
        },
        computeParetoFront(data){
            // need pairs of x,y values
            let points = []
            for (let i = 0; i < data.challenge_participants.length; i++) {
                let point = [data.challenge_participants[i].metric_x, data.challenge_participants[i].metric_y]
                points.push(point)
            }
            return pf.getParetoFrontier(points, { optimize: paretoMappings[data.visualization.optimization]});
            
        }
    }
}


</script>