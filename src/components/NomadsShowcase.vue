<template>
  <section class="nomads-showcase-section">
    <div class="showcase-header">
      <div class="header-left">
        <h2 class="showcase-title">AIGC 降重与学术润色实战模板库</h2>
        <p class="showcase-subtitle">精选高频学术降重与润色场景，点击“一键套用”快速生成高质量对比报告</p>
      </div>
      <span class="showcase-badge">已收录 {{ showcaseItems.length }} 个经典案例</span>
    </div>

    <div class="showcase-grid">
      <div 
        v-for="item in showcaseItems" 
        :key="item.id" 
        class="glass-card showcase-card"
      >
        <div class="card-header">
          <span class="scenario-tag">{{ item.tag }}</span>
          <span class="usage-count">{{ item.usageCount }} 次应用</span>
        </div>

        <div class="card-content">
          <h3 class="item-title">{{ item.title }}</h3>
          <p class="item-prompt">“{{ item.prompt }}”</p>
        </div>

        <div class="card-action">
          <button class="apply-btn" @click="applyTemplate(item)">
            <span>一键套用</span>
            <svg class="arrow-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <line x1="5" y1="12" x2="19" y2="12"></line>
              <polyline points="12 5 19 12 12 19"></polyline>
            </svg>
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { computed } from 'vue';

const emit = defineEmits<{
  (e: 'apply-template', payload: { prompt: string; mode?: string; subject?: string }): void;
}>();

export interface ShowcaseItem {
  id: string;
  tag: string;
  title: string;
  prompt: string;
  mode?: string;
  subject?: string;
  usageCount: string;
}

const showcaseItems = computed<ShowcaseItem[]>(() => [
  {
    id: 'aigc-1',
    tag: '工学技术',
    title: '深度学习算法段落去AI特征',
    prompt: '此外，不可否认的是，卷积神经网络在特征提取方面表现出了巨大的优越性。总而言之，我们提出的改进模型能够显著提高图像识别的准确率。',
    mode: '重度降重去AI痕迹',
    subject: '工学技术',
    usageCount: '38.2k'
  },
  {
    id: 'aigc-2',
    tag: '医学医药',
    title: '临床对照实验结论学术润色',
    prompt: '实验结果表明，该药物对于降低患者血压具有非常好的效果，并且没有明显的毒副作用。所以我们认为这种疗法值得在临床上推广。',
    mode: '顶刊学术语体润色',
    subject: '医学医药',
    usageCount: '29.5k'
  },
  {
    id: 'aigc-3',
    tag: '经济管理',
    title: '面板数据计量回归分析逻辑重构',
    prompt: '由于数字经济的快速发展，企业创新绩效得到了极大的提升。另外，市场竞争程度在其中起到了中介作用，使得效应更加明显。',
    mode: '逻辑衔接与结构强化',
    subject: '经济管理',
    usageCount: '34.1k'
  },
  {
    id: 'aigc-4',
    tag: '人文社科',
    title: '质性研究文献综述去AI套话',
    prompt: '随着全球化进程的不断深入，文化认同问题成为了学术界关注的热点。众所周知，不同文化之间的碰撞与融合产生了深刻的影响。',
    mode: '重度降重去AI痕迹',
    subject: '人文社科',
    usageCount: '27.9k'
  },
  {
    id: 'aigc-5',
    tag: '理学基础',
    title: '量子物理机理推导学术改写',
    prompt: '通过对波函数的解算，我们可以发现粒子在特定能级上的分布规律。这一发现对于理解微观粒子的跃迁机制具有十分关键的意义。',
    mode: '顶刊学术语体润色',
    subject: '理学基础',
    usageCount: '19.8k'
  },
  {
    id: 'aigc-6',
    tag: '查重改写',
    title: '高查重率重复段落同义置换',
    prompt: '本文采用问卷调查法对消费者的购买意愿进行了实证分析，统计结果验证了之前的假设，证明信任度对购买决策有正向作用。',
    mode: '查重报告针对性改写',
    subject: '经济管理',
    usageCount: '41.6k'
  }
]);

function applyTemplate(item: ShowcaseItem) {
  emit('apply-template', {
    prompt: item.prompt,
    mode: item.mode,
    subject: item.subject
  });
}
</script>

<style scoped>
.nomads-showcase-section {
  margin-top: 2rem;
  width: 100%;
}

.showcase-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  margin-bottom: 1.25rem;
  padding-bottom: 0.75rem;
  border-bottom: 1px solid var(--card-border);
}

.showcase-title {
  font-size: 1.2rem;
  font-weight: 700;
  color: var(--text-primary);
  background: var(--primary-gradient);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.showcase-subtitle {
  font-size: 0.825rem;
  color: var(--text-secondary);
  margin-top: 0.25rem;
}

.showcase-badge {
  font-size: 0.75rem;
  color: #a5b4fc;
  background: rgba(99, 102, 241, 0.12);
  border: 1px solid rgba(99, 102, 241, 0.25);
  padding: 4px 10px;
  border-radius: 20px;
}

.showcase-grid {
  display: grid;
  grid-template-columns: repeat(1, 1fr);
  gap: 1.25rem;
}

@media (min-width: 640px) {
  .showcase-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (min-width: 1024px) {
  .showcase-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}

.showcase-card {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100%;
  padding: 1.25rem;
  background: rgba(255, 255, 255, 0.02);
  border: 1px solid var(--card-border);
  border-radius: 14px;
  transition: all 0.25s ease;
}

.showcase-card:hover {
  background: rgba(255, 255, 255, 0.05);
  border-color: rgba(99, 102, 241, 0.4);
  transform: translateY(-3px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.4);
}

.card-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 0.75rem;
}

.scenario-tag {
  font-size: 0.75rem;
  font-weight: 600;
  padding: 3px 8px;
  border-radius: 6px;
  background: rgba(168, 85, 247, 0.15);
  color: #c084fc;
  border: 1px solid rgba(168, 85, 247, 0.3);
}

.usage-count {
  font-size: 0.75rem;
  color: var(--text-secondary);
}

.card-content {
  margin-bottom: 1rem;
  flex: 1;
}

.item-title {
  font-size: 0.95rem;
  font-weight: 600;
  color: var(--text-primary);
  margin-bottom: 0.4rem;
}

.item-prompt {
  font-size: 0.825rem;
  color: var(--text-secondary);
  line-height: 1.45;
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  overflow: hidden;
  font-style: italic;
}

.card-action {
  padding-top: 0.75rem;
  border-top: 1px solid rgba(255, 255, 255, 0.04);
}

.apply-btn {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 6px;
  padding: 0.5rem 1rem;
  background: rgba(99, 102, 241, 0.1);
  border: 1px solid rgba(99, 102, 241, 0.3);
  border-radius: 8px;
  color: #a5b4fc;
  font-size: 0.825rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.2s ease;
}

.showcase-card:hover .apply-btn {
  background: var(--primary-gradient);
  border-color: transparent;
  color: white;
}

.arrow-icon {
  width: 14px;
  height: 14px;
  transition: transform 0.2s ease;
}

.apply-btn:hover .arrow-icon {
  transform: translateX(3px);
}
</style>
