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
    title: {
      text: 'Referer of a Website',
      subtext: 'Fake Data',
      left: 'center',
    },
    tooltip: {
      trigger: 'item',
    },
    legend: {
      orient: 'vertical',
      left: 'left',
    },
    series: [
      {
        name: 'Access From',
        type: 'pie',
        radius: '50%',
        data: [
          { value: 1048, name: 'Search Engine' },
          { value: 735, name: 'Direct' },
          { value: 580, name: 'Email' },
          { value: 484, name: 'Union Ads' },
          { value: 300, name: 'Video Ads' },
        ],
        emphasis: {
          itemStyle: {
            shadowBlur: 10,
            shadowOffsetX: 0,
            shadowColor: 'rgba(0, 0, 0, 0.5)',
          },
        },
      },
    ],
  })
})
</script>
