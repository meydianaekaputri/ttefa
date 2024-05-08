<script setup lang="ts">
import Chart from 'chart.js/auto';

const labels = [
    'Januari',
    'Februari',
    'March',
    'April',
    'May',
    'June',
];

    const data = {
        labels: labels,
        datasets: [{
            label: 'My First dataset',
            backgroundColor: '#C0C0C0',
            borderColor: 'rgb(2555, 99, 132)',
            data: [10, 15, 30, 10, 20, 30, 45],
        }]
    };

    const config = {
        type: 'bar',
        data: data,
        Options: {}
    };

onMounted(() => {
    const myChart = new Chart (
        document.getElementById('myChart'),
        config
    );
})
</script>

<template>
    <div>
        <canvas id="myChart"></canvas>
    </div>
</template>