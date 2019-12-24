<template>
  <div id="app">
    <h1>LineChart</h1>
    <LineChart
      :data="{
        labels: [
          'January',
          'February',
          'March',
          'April',
          'May',
          'June',
          'July'
        ],
        datasets: [
          {
            label: 'Data One',
            backgroundColor: '#f87979',
            data: [40, 39, 10, 40, 39, 80, 40]
          }
        ]
      }"
      :options="{ responsive: true, maintainAspectRatio: false }"
    />

    <hr />
    <h1>BarChart</h1>
    <BarChart
      :data="{
        labels: [
          'January',
          'February',
          'March',
          'April',
          'May',
          'June',
          'July'
        ],
        datasets: [
          {
            label: 'Data One',
            backgroundColor: [
              '#ff6384',
              '#36a2eb',
              '#cc65fe',
              '#ffce56',
              'red',
              'green',
              'blue'
            ],
            data: [40, 39, 20, 40, 39, 80, 40]
          }
        ]
      }"
      :options="{
        responsive: true,
        maintainAspectRatio: false,
        scales: {
          yAxes: [
            {
              ticks: {
                min: 0,
                stepSize: 5
              }
            }
          ]
        }
      }"
    />

    <hr />
    <h1>PieChart</h1>
    <PieChart
      :data="{
        labels: [
          'January',
          'February',
          'March',
          'April',
          'May',
          'June',
          'July'
        ],
        datasets: [
          {
            label: 'Data One',
            backgroundColor: [
              '#ff6384',
              '#36a2eb',
              '#cc65fe',
              '#ffce56',
              'red',
              'green',
              'blue'
            ],
            data: [40, 39, 10, 40, 39, 80, 40]
          }
        ]
      }"
      :options="{ responsive: true, maintainAspectRatio: false }"
    />

    <hr />
    <h1>PieChart - Multiple</h1>
    <PieChart
      :data="{
        labels: [
          'January',
          'February',
          'March',
          'April',
          'May',
          'June',
          'July'
        ],
        datasets: [
          {
            label: 'Data One',
            backgroundColor: [
              '#ff6384',
              '#36a2eb',
              '#cc65fe',
              '#ffce56',
              'red',
              'green',
              'blue'
            ],
            borderColor: '#777',
            borderWidth: 0,
            data: [40, 39, 10, 40, 39, 80, 40]
          },
          {
            label: 'Data Two',
            backgroundColor: ['red', 'green'],
            borderColor: 'white',
            borderWidth: 2,
            data: [22, 55]
          },
          {
            label: 'Data Three',
            backgroundColor: ['blue', 'yellow'],
            borderColor: '#777',
            borderWidth: 5,
            data: [11, 66]
          }
        ]
      }"
      :options="{ responsive: true, maintainAspectRatio: false }"
    />

    <hr />
    <h1>DoughnutChart</h1>
    <DoughnutChart
      :data="{
        labels: [
          'January',
          'February',
          'March',
          'April',
          'May',
          'June',
          'July'
        ],
        datasets: [
          {
            label: 'Data One',
            backgroundColor: [
              '#ff6384',
              '#36a2eb',
              '#cc65fe',
              '#ffce56',
              'red',
              'green',
              'blue'
            ],
            borderColor: '#fff',
            borderWidth: 2,
            data: [40, 39, 10, 40, 39, 80, 40]
          }
        ]
      }"
      :options="{ responsive: true, maintainAspectRatio: false }"
    />
  </div>
</template>

<script>
import LineChart from "./components/Charts/Chartjs/LineChart.vue";
import BarChart from "./components/Charts/Chartjs/BarChart.vue";
import PieChart from "./components/Charts/Chartjs/PieChart.vue";
import DoughnutChart from "./components/Charts/Chartjs/DoughnutChart.vue";

export default {
  name: "app",
  components: {
    LineChart,
    BarChart,
    PieChart,
    DoughnutChart
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
