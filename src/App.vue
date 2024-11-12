<template>
  <h1>Echarts Vue</h1>
  <div>
    <details>
      <summary>ECharts入门示例</summary>
      <div class="chart-wrapper">
        <GettingStarted />
      </div>
    </details>

    <details>
      <summary>基础折线图</summary>
      <div class="chart-wrapper">
        <BasicLineChart />
      </div>
    </details>

    <details>
      <summary>基础柱状图</summary>
      <div class="chart-wrapper">
        <BasicBar />
      </div>
    </details>

    <details>
      <summary>某站点用户Access From</summary>
      <div class="chart-wrapper">
        <RefererOfAWebsite />
      </div>
    </details>
  </div>
</template>

<script setup>
import BasicBar from './components/bar/BasicBar.vue'
import GettingStarted from './components/GettingStarted.vue'
import BasicLineChart from './components/line/BasicLineChart.vue'
import RefererOfAWebsite from './components/pie/RefererOfAWebsite.vue'
</script>

<style scoped>
.chart-wrapper > div {
  width: 600px;
  height: 400px;
}
</style>
