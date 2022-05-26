<script setup>
import { onMounted, ref } from 'vue'
import Chart from '@/chart' 

const data = {
  labels:  [
    'January',
    'February',
    'March',
    'April',
    'May',
    'June',
    'July',
],
  datasets: [{
    label: 'My First Dataset',
    data: [65, 59, 80, 81, 56, 55, 40],
    fill: false,
    borderColor: 'rgb(75, 192, 192)',
    tension: 0.1
  }]
};
const config = {
    type: 'line',
    data: data,
};
const chartElement = ref()
onMounted(
() => {
    const myChart = new Chart(
    chartElement.value,
    config
    );
}
)
</script>

<template>
<div>
    <canvas ref="chartElement"></canvas>
</div>
</template>

<style>
</style>
