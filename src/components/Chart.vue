<template>
<div>
  <div class="chart-wrapper">
        <chart :options="chartOptionsBar"></chart>
  </div>
  <hr/>
  <div class="chart-wrapper">
    <chart :options="chartOptionsLine"></chart>
  </div>
</div>
  
</template>

<script>
export default {
 
  data: () => ({
   chartOptionsBar: {
      xAxis: {
      data: ['First', 'Second', 'Third','Fourth']
    },
    yAxis: {
      type: 'value'
    },
    series: [
      {
        type: 'bar',
        data: [78, 90, 24,12]
      }
    ],
    title: {
      text: 'Quater sales Results',
      x: 'center',
      textStyle: {
        fontSize: 24
      }
    },
     color: ['#127ac2']
   },
   chartOptionsLine: {
     xAxis: {
       data: [
          "Jan",
          "Feb",
          "Mar",
          "Apr",
          "May",
          "Jun",
          "Jul",
          "Aug",
          "Sep",
          "Oct",
          "Nov",
          "Dec"
       ]
     },
     yAxis: {
       type: 'value'
     },
     series: [
       {
         type: 'line',
         data: [55, 72, 84, 48, 59, 62, 87, 75, 94, 101, 127, 118]
       }
     ],
     title: {
       text: 'Monthly Stock Prices',
       x: 'center',
       textStyle: {
         fontSize: 24
       }
     },
     color: ['#127ac2']
   }
  })
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .chart-wrapper {
    widows: 100%;
    height: 700px;
    margin-bottom: 40px;
  }

  .echarts {
    width: 100%;
    height: 100%;
  }
</style>
