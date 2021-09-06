<template>
    <el-container>
        <el-main>

            <h3>告警统计</h3>
            <div class="chart-box2">
                <lineChart class="chart"></lineChart>
            </div>
            <h3>规则统计</h3>
            <div class="chart-box1">
                <pieChart class="chart"></pieChart>
                <pieChart class="chart"></pieChart>
                <pieChart class="chart"></pieChart>
                <pieChart class="chart"></pieChart>
            </div>
            <h3>触发器统计</h3>
            <div class="chart-box1">
                <pieChart class="chart"></pieChart>
                <pieChart class="chart"></pieChart>
                <pieChart class="chart"></pieChart>
                <pieChart class="chart"></pieChart>
            </div>
            <h3>接入统计</h3>
            <div class="chart-box1">
                <pieChart class="chart"></pieChart>
                <pieChart class="chart"></pieChart>
                <pieChart class="chart"></pieChart>
                <pieChart class="chart"></pieChart>
            </div>
        </el-main>
    </el-container>
</template>

<script>
import pieChart from './pieChart.vue';
import lineChart from './lineChart.vue';

export default {
    components:{
        pieChart,
        lineChart
    }
}
</script>

<style scoped>
    .el-container{
        height:calc(100vh - 80px);
    }
    .el-main{
        overflow-x: hidden;
    }    

    .chart-box1{
        width: 100%;
        height: 300px;
        display: flex;
        flex-wrap: nowrap;
    }
    .chart-box1 > .chart{
        width:50%;
        height:100%;
        background:#f2f2f2;
    }
    h3{
        padding: 10px 0px 0px 10px;
    }

    .chart-box2{
        width: 100%;
        height: 300px;
        padding: 20px 0px 50px 0px;
        background: #f2f2f2;
        
    }
    .chart-box2 > .chart{
        width:100%;
        height:100%;
    }
</style>