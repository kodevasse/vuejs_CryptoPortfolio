<template>
  <article
    class="animate-background rounded-xl bg-gradient-to-r from-green-300 via-orange-500 to-purple-500 bg-[length:400%_400%] p-0.5 shadow-xl transition [animation-duration:_6s] hover:shadow-sm dark:shadow-gray-700/25"
  >
    <div
      class="rounded-[10px] bg-white p-4 dark:bg-gray-900 sm:p-6 flex items-center flex-col"
    >
      <h3
        class="font-extrabold text-transparent text-2xl bg-clip-text bg-gradient-to-r from-emerald-100 to-pink-400"
      >
        Crypto portfolio 23
      </h3>

      <div class="mt-4 flex flex-wrap gap-1">
        <BarChart />
      </div>
    </div>
  </article>
</template>

<script setup>
import BarChart from "@/components/BarChart.vue";
</script>
