<script setup>
import { onMounted, ref } from 'vue'
import { Chart,  LineController, LineElement, PointElement, LinearScale, Title, CategoryScale} from 'chart.js' 
Chart.register(LineController, LineElement, PointElement, LinearScale, Title, CategoryScale);
const labels = [
    'January',
    'February',
    'March',
    'April',
    'May',
    'June',
  ];

  const data = {
    labels: labels,
    datasets: [{
      label: 'My First dataset',
      backgroundColor: 'rgb(255, 99, 132)',
      borderColor: 'rgb(255, 99, 132)',
      data: [0, 10, 5, 2, 20, 30, 45],
    }]
  };

  const config = {
    type: 'line',
    data: data,
    options: {}
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
