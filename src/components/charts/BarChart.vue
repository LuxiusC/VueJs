<script setup>
import { Bar } from "vue-chartjs"
import {Chart as ChartJS, Title, Legend, BarElement, CategoryScale, LinearScale} from 'chart.js'

const {data} = defineProps(['data'])

//Register chart functionality
ChartJS.register(Title, Legend, BarElement, CategoryScale, LinearScale)

const options = {responsive:true}


</script>

<template>
 <div>
    <Bar id="my-chart" :options="options" :data="data">
    
    </Bar>
 </div>
</template>