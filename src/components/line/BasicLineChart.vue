<template>
  <div ref="main"></div>
</template>

<script setup>
import * as echarts from 'echarts'
import { onMounted, useTemplateRef } from 'vue'

const mainRef = useTemplateRef('main')

onMounted(() => {
  // 基于准备好的dom，初始化echarts实例
  var myChart = echarts.init(mainRef.value)

  // 绘制图表
  myChart.setOption({
    xAxis: {
      type: 'category',
      data: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun'],
    },
    yAxis: {
      type: 'value',
    },
    series: [
      {
        data: [150, 230, 224, 218, 135, 147, 260],
        type: 'line',
      },
    ],
  })
})
</script>
