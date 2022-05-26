<script setup>
import barChart from '@/charts/bar-chart.vue'
import doughnutChart from '@/charts/doughnut-chart.vue'
import lineChart from '@/charts/line-chart.vue'
</script>

<template>
  <div class="chart-container">
    <bar-chart />
  </div>
  <div class="chart-container">
    <doughnut-chart />
  </div>
  <div class="chart-container">
    <line-chart />
  </div>
</template>

<style scoped>
.chart-container {
  position: relative; 
  height:400px; 
  width:400px;
  display:inline-block
}
</style>