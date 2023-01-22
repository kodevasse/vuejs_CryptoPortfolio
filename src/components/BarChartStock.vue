<template>
  <Doughnut id="my-chart-id" :options="chartOptions" :data="chartData" />
</template>

<script>
import { Doughnut } from "vue-chartjs";
import { Chart as ChartJS, Title, Tooltip, ArcElement, Legend } from "chart.js";

ChartJS.register(Title, Tooltip, ArcElement, Legend);

export default {
  name: "BarChart2",
  components: { Doughnut },
  data() {
    return {
      chartData: {
        labels: [
          "Global Index Fund",
          "China Index Fund",
          "India Index Fund",
          "Oil & Gas Index Fund",

          "Environmental Stocks",
          "5AI Stocks",
        ],
        options: {
          legend: {
            labels: {
              fontColor: "white",
            },
          },
        },
        datasets: [
          {
            backgroundColor: [
              "rgba(14, 119, 178)",
              "rgba(236, 72, 153)",
              "rgba(210, 235, 52)",
              "rgba(74, 222, 128)",
              "rgba(120, 113, 108)",
              "rgba(233, 213, 255)",
              "rgba(250, 204, 21)",
            ],
            borderColor: "rgb(17 24 39)",
            borderWidth: 5,
            tension: 0.1,
            pointRadius: 0.5,
            // fill: false

            data: [51, 13, 11, 15, 5, 5],
          },
        ],
        hoverOffset: 4,
      },
      chartOptions: {
        responsive: true,

        // maintainAspectRatio: false,
      },
    };
  },
};
</script>

<style scoped></style>
