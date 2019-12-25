<template>
  <div id="app">
    <h1>LineChart</h1>
    <LineChart :data="myLineData" :options="myLineOptions" />

    <hr />
    <h1>BarChart</h1>
    <BarChart :data="myBarData" :options="myBarOptions" />

    <hr />
    <h1>HorizontalBarChart</h1>
    <HorizontalBarChart :data="myBarData" :options="myBarOptions" />

    <hr />
    <h1>PieChart</h1>
    <PieChart :data="myPieData" :options="myPieOptions" />

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
    <DoughnutChart :data="myDoughnutData" :options="myDoughnutOptions" />

    <hr />
    <h1>BubbleChart</h1>
    <BubbleChart :data="myBubbleData" :options="myBubbleOptions" />

    <hr />
    <h1>ScatterChart</h1>
    <ScatterChart :data="myScatterData" :options="myScatterOptions" />
  </div>
</template>

<script>
import LineChart from "./components/Charts/Chartjs/LineChart.vue";
import BarChart from "./components/Charts/Chartjs/BarChart.vue";
import HorizontalBarChart from "./components/Charts/Chartjs/HorizontalBarChart.vue";
import PieChart from "./components/Charts/Chartjs/PieChart.vue";
import DoughnutChart from "./components/Charts/Chartjs/DoughnutChart.vue";
import BubbleChart from "./components/Charts/Chartjs/BubbleChart.vue";
import ScatterChart from "./components/Charts/Chartjs/ScatterChart.vue";

export default {
  name: "app",
  components: {
    LineChart,
    BarChart,
    HorizontalBarChart,
    PieChart,
    DoughnutChart,
    BubbleChart,
    ScatterChart
  },
  data() {
    return {
      myLineData: {
        labels: [
          "January",
          "February",
          "March",
          "April",
          "May",
          "June",
          "July"
        ],
        datasets: [
          {
            label: "Data One",
            borderColor: "#f87979",
            backgroundColor: "rgba(255, 0, 0, 0.2)",
            data: [40, 39, 10, 40, 39, 80, 40]
          },
          {
            label: "Data Two",
            borderColor: "#79f879",
            backgroundColor: "rgba(0, 255, 0, 0.2)",
            data: [39, 10, 40, 39, 80, 100, 22]
          }
        ]
      },
      myLineOptions: {
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
      },

      myBarData: {
        labels: [
          "January",
          "February",
          "March",
          "April",
          "May",
          "June",
          "July"
        ],
        datasets: [
          {
            label: "Data One",
            backgroundColor: [
              "#ff6384",
              "#36a2eb",
              "#cc65fe",
              "#ffce56",
              "red",
              "green",
              "blue"
            ],
            data: [40, 39, 20, 40, 39, 80, 40],
            rough: {
              fillStyle: "cross-hatch",
              hachureGap: 8
            }
          },
          {
            label: "Data Two",
            borderColor: "#79f879",
            backgroundColor: [
              "#ffce56",
              "red",
              "green",
              "blue",
              "#ff6384",
              "#36a2eb",
              "#cc65fe"
            ],
            data: [39, 10, 40, 39, 80, 100, 22],
            rough: {
              fillStyle: "cross-hatch",
              hachureGap: 8
            }
          },
          {
            label: "Data Three",
            borderColor: "#79f879",
            backgroundColor: [
              "blue",
              "#ff6384",
              "#36a2eb",
              "red",
              "green",
              "#cc65fe",
              "#ffce56"
            ],
            data: [29, 40, 10, 69, 10, 30, 92],
            rough: {
              fillStyle: "cross-hatch",
              hachureGap: 8
            }
          }
        ]
      },
      myBarOptions: {
        responsive: true,
        maintainAspectRatio: false,
        scales: {
          xAxes: [
            {
              scaleLabel: {
                display: true,
                labelString: "My X-axis Label"
              }
            }
          ],
          yAxes: [
            {
              ticks: {
                min: 0,
                stepSize: 5
              },
              scaleLabel: {
                display: true,
                labelString: "My Y-axis Label"
              }
            }
          ]
        },
        plugins: {
          rough: {
            enabled: true
          }
        }
      },

      myPieData: {
        labels: [
          "January",
          "February",
          "March",
          "April",
          "May",
          "June",
          "July"
        ],
        datasets: [
          {
            label: "Data One",
            backgroundColor: [
              "#ff6384",
              "#36a2eb",
              "#cc65fe",
              "#ffce56",
              "red",
              "green",
              "blue"
            ],
            data: [40, 39, 10, 40, 39, 80, 40]
          }
        ]
      },
      myPieOptions: {
        responsive: true,
        maintainAspectRatio: false
      },

      myDoughnutData: {
        labels: [
          "January",
          "February",
          "March",
          "April",
          "May",
          "June",
          "July"
        ],
        datasets: [
          {
            label: "Data One",
            backgroundColor: [
              "#ff6384",
              "#36a2eb",
              "#cc65fe",
              "#ffce56",
              "red",
              "green",
              "blue"
            ],
            borderColor: "#fff",
            borderWidth: 2,
            data: [40, 39, 10, 40, 39, 80, 40]
          }
        ]
      },
      myDoughnutOptions: {
        responsive: true,
        maintainAspectRatio: false
      },

      myBubbleData: {
        labels: [
          "January",
          "February",
          "March",
          "April",
          "May",
          "June",
          "July"
        ],
        datasets: [
          {
            label: "Data One",
            hoverBackgroundColor: "#ff6384",
            hoverRadius: 2,
            backgroundColor: [
              "#ff6384",
              "#36a2eb",
              "#cc65fe",
              "#ffce56",
              "red",
              "green",
              "blue"
            ],
            data: [
              {
                x: 20,
                y: 40,
                r: 4
              },
              {
                x: 60,
                y: 60,
                r: 30
              },
              {
                x: 30,
                y: 70,
                r: 50
              },
              {
                x: 40,
                y: 80,
                r: 10
              },
              {
                x: 50,
                y: 80,
                r: 30
              }
            ]
          }
        ]
      },
      myBubbleOptions: {
        responsive: true,
        maintainAspectRatio: false
      },

      myScatterData: {
        labels: [
          "January",
          "February",
          "March",
          "April",
          "May",
          "June",
          "July"
        ],
        datasets: [
          {
            label: "Data One",
            backgroundColor: [
              "#ff6384",
              "#36a2eb",
              "#cc65fe",
              "#ffce56",
              "green",
              "blue"
            ],
            borderColor: "#fff",
            borderWidth: 2,
            pointRadius: 10,
            pointHoverRadius: 15,
            data: [
              {
                x: -10,
                y: 0
              },
              {
                x: 0,
                y: 10
              },
              {
                x: 10,
                y: 5
              },
              {
                x: 40,
                y: 80
              },
              {
                x: 50,
                y: 20
              }
            ]
          }
        ]
      },
      myScatterOptions: {
        responsive: true,
        maintainAspectRatio: false,
        scales: {
          xAxes: [
            {
              type: "linear",
              position: "bottom"
            }
          ]
        }
      }
    };
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
