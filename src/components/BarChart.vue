<template>
  <Doughnut id="my-chart-id" :options="chartOptions" :data="chartData" />
</template>

<script>
import { Doughnut } from "vue-chartjs";
import { Chart as ChartJS, Title, Tooltip, ArcElement, Legend } from "chart.js";

ChartJS.register(Title, Tooltip, ArcElement, Legend);

export default {
  name: "BarChart",
  components: { Doughnut },
  data() {
    return {
      chartData: {
        labels: [
          "Btc",
          "Polkadot",
          "Azero",
          "Ethereum",
          "L2 scaling",
          "Others L1",
          "Altcoins 50+",
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
              "rgba(239,68,68)",
              "rgba(236, 72, 153)",
              "rgba(8, 145, 178)",
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

            data: [12, 30, 10, 20, 8, 10, 10],
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
