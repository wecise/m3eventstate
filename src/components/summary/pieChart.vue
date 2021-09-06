<template>
    <div style="height:100%;">
        <h5></h5>
        <v-chart :option="option" 
            class="chart" 
            :autoresize="true"
            style="height:100%;">
        </v-chart>
    </div>
</template>

<script>
import _ from 'lodash';
import ECharts  from "vue-echarts";
import { use } from 'echarts/core';

import {
  CanvasRenderer,
} from 'echarts/renderers'
import {
  PieChart
} from 'echarts/charts';
import {
  GridComponent,
  TooltipComponent,
  LegendComponent
} from 'echarts/components';

use([
  CanvasRenderer,
  PieChart,
  GridComponent,
  TooltipComponent,
  LegendComponent
]);

export default{
    props: {
        model: Object
    },
    components: {
        "v-chart": ECharts
    },
    data() {
        return {
            option: {
                tooltip: {
                    trigger: 'item'
                },
                legend: {
                    top: '5%',
                    left: 'center'
                },
                series: [
                    {
                        name: '告警统计',
                        type: 'pie',
                        radius: ['40%', '70%'],
                        avoidLabelOverlap: false,
                        itemStyle: {
                            borderRadius: 10,
                            borderColor: '#fff',
                            borderWidth: 2
                        },
                        label: {
                            show: false,
                            position: 'center'
                        },
                        emphasis: {
                            label: {
                                show: true,
                                fontSize: '40',
                                fontWeight: 'bold'
                            }
                        },
                        labelLine: {
                            show: false
                        },
                        data: [
                            {value: 48, name: '一般告警'},
                            {value: 735, name: '严重告警'},
                            {value: 580, name: '重大高级'}
                        ]
                    }
                ]
            }
        };
    },
    mounted() {

    },
    methods: {
        
        
    }  
}
</script>
