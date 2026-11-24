<script setup>
import { Line } from 'vue-chartjs';
import {Chart as ChartJS, LinearScale, CategoryScale, Title, Legend, LineElement,PointElement} from "chart.js"

ChartJS.register(LinearScale, CategoryScale, Title, Legend, LineElement,PointElement)

const {data,title} = defineProps(['data','title'])
const option = {
    responsive:"true",
    plugins:{
    title:{
        display:true,
        text:title
    }
    }
}

</script>

<template>
<div>
    <Line id="line-chart" :data="data" :options="option"/>
</div>
</template>