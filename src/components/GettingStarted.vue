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
    tooltip: {},
    xAxis: {
      data: ['衬衫', '羊毛衫', '雪纺衫', '裤子', '高跟鞋', '袜子'],
    },
    yAxis: {},
    series: [
      {
        name: '销量',
        type: 'bar',
        data: [5, 20, 36, 10, 10, 20],
      },
    ],
  })
})
</script>
