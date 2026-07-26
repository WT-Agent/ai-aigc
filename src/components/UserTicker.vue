<template>
  <div class="glass-card ticker-card">
    <div class="ticker-wrapper">
      <div v-for="(item, index) in tickerItems" :key="index" class="ticker-item">
        <span>{{ item.text }}</span>
        <span style="color: var(--success-color); font-weight: bold;">[重构降重成功]</span>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const tickerItems = ref([
  { text: '用户 135****4829 完成了工学毕业论文 AIGC 痕迹降重' },
  { text: '用户 173****9238 完成了 SCI 期刊论文顶刊语体润色' },
  { text: '用户 189****1102 完成了医学综述逻辑结构与因果衔接强化' },
  { text: '用户 130****8739 完成了经管类开题报告同义词替换与去AI化' },
  { text: '用户 152****2394 完成了人文社科课程论文查重针对性改写' },
]);
</script>
