<script setup>
import barChart from '@/charts/bar-chart.vue'
import doughnutChart from '@/charts/doughnut-chart.vue'
import lineChart from '@/charts/line-chart.vue'
</script>

<template>
  <div class="container">
    <div class="chart-container">
      <bar-chart />
    </div>
    <div class="chart-container" style="width:500px">
      <doughnut-chart />
    </div>
    <div class="chart-container">
      <line-chart />
    </div>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  width: 100%;
}
.chart-container {
  width: 800px;
  margin:50px
}
</style>