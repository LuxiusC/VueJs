<script setup>
import BarChart from './components/charts/BarChart.vue';
import LineChart from './components/charts/LineChart.vue';
const data = {
  labels: ["A","B","C","D"],
  datasets:[
  {
    label:"My Chart",
    backgroundColor:"#087e8B",
    data:[500,350,900,750]
  },
  {
    label:"My Chart",
    backgroundColor:"#FF5A5F",
    data:[400,150,200,650]
  }
  ]
}


</script>

<template>

  <div class="flex flex-col gap-y-4 p-8">
    <h1 class="text-2xl">Bar Chart</h1>
    <BarChart :data="data" class="chart"/>
    <h1 class="text-2xl">Line Chart</h1>
    <LineChart title="MY LINE CHART":data="data" class="chart"/>
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.chart{
  height:500px;
  width:500px;
}


.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
