<template>
    <div class="chart">
        <h1>Chart</h1>
        <DxChart
      id="chart"
      :data-source="dataSource"
    >
      <DxSeries
        argument-field="day"
        value-field="oranges"
        name="My oranges"
        type="bar"
        color="#ffaa66"
      />
    </DxChart>

    </div>
  </template>
  <script lang="ts">
  import { DxChart, DxSeries } from 'devextreme-vue/chart';

  const dataSource = [{
    day: 'Monday',
    oranges: 3,
  }, {
    day: 'Tuesday',
    oranges: 2,
  }, {
    day: 'Wednesday',
    oranges: 3,
  }, {
    day: 'Thursday',
    oranges: 4,
  }, {
    day: 'Friday',
    oranges: 6,
  }, {
    day: 'Saturday',
    oranges: 11,
  }, {
    day: 'Sunday',
    oranges: 4,
  }];
  export default {
    components: {
      DxChart,
      DxSeries,
    },
    data() {
      return {
        dataSource,
      };
    },
  };
  </script>
  <style>
    .chart{
        width: 70rem;
        padding: 1rem;
        margin: 5rem;
        margin-left: 10rem;
        background-color:  rgba(255, 255, 255, 0.8);
    }

  #chart {
    height: 440px;
  }

  .chart h1{
    font-size: 50px;
  }
  </style>