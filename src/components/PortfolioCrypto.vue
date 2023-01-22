<template>
  <div class="gap-x-10 gap-y-8 flex sm:flex-row flex-col">
    <article
      class="animate-background max-w-3xl rounded-xl bg-gradient-to-r from-cyan-300 via-slate-300 to-amber-500 bg-[length:400%_400%] p-0.5 shadow-xl transition [animation-duration:_6s] hover:shadow-sm dark:shadow-gray-600/25"
    >
      <div
        class="rounded-[10px] bg-white p-4 dark:bg-gray-900 sm:p-6 flex items-center flex-col"
      >
        <h3
          class="font-extrabold text-transparent text-2xl bg-clip-text bg-gradient-to-r from-amber-300 to-pink-400"
        >
          Crypto
        </h3>

        <div class="mt-4 flex flex-wrap gap-5">
          <BarChart />
        </div>
      </div>
    </article>
    <article
      class="animate-background max-w-3xl rounded-xl bg-gradient-to-r from-green-300 via-orange-500 to-purple-500 bg-[length:400%_400%] p-0.5 shadow-xl transition [animation-duration:_6s] hover:shadow-sm dark:shadow-gray-600/25"
    >
      <div
        class="h-full rounded-[10px] bg-white p-4 dark:bg-gray-900 sm:p-6 flex items-center flex-col"
      >
        <h3
          class="font-extrabold text-transparent text-2xl bg-clip-text bg-gradient-to-r from-cyan-200 to-amber-400"
        >
          Stock/Fund
        </h3>
        <BarChartStock />
        <div class="mt-4 flex flex-wrap gap-1"></div>
      </div>
    </article>
  </div>
</template>

<script setup>
import BarChart from "@/components/BarChart.vue";
import BarChartStock from "@/components/BarChartStock.vue";
</script>
