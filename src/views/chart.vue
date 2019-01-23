<template>
    <div class="chart">
        <h1>Vue-Chart-demo</h1>
        <div  class="grid">
            <ChartBar/>
            <ChartDoughunt/>
            <ChartLine/> 
        </div>
    </div>
</template>

<script>
import ChartBar from "@/components/chart-bar";
import ChartDoughunt from "@/components/chart-doughunt";
import ChartLine from "@/components/chart-Line";

export default {
    comments: {
        ChartBar,
        ChartDoughunt,
        ChartLine
    }
};
</script>

<style>
@import url(./CSS/all.min.css);
    .grid {
    display: grid;
    row-gap: 2rem;
    }
</style>
