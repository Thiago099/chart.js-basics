<script setup>
import { onMounted, ref } from 'vue'
import Chart from '@/chart' 
const data = {
labels: [
    'Red',
    'Blue',
    'Yellow'
],
datasets: [{
    label: 'My First Dataset',
    data: [300, 50, 100],
    backgroundColor: [
    'rgb(255, 99, 132)',
    'rgb(54, 162, 235)',
    'rgb(255, 205, 86)'
    ],
    hoverOffset: 4
}]
};
const config = {
    type: 'doughnut',
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
