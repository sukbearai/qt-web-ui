<script lang="ts" setup>
import Progress from './Progress.vue'

const { env1, env2, startDynamicUpdate } = useDynamicMockData()

startDynamicUpdate()

const size = ref(80)
</script>

<template>
  <div class="flex justify-around">
    <div class="flex flex-col items-center text-[#fff]">
      <Progress :width="size" :height="size" :text="`${env1}°C`" :percent="env1" />
      <div>温度</div>
    </div>
    <div class="flex flex-col items-center text-center text-[#fff]">
      <Progress :width="size" :height="size" :text="`${env2} %`" :percent="env2" />
      <div>湿度</div>
    </div>
  </div>
</template>
