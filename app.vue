<template>
  <div>
    <NuxtRouteAnnouncer />
    <Background />
    <div class="secions">
      <TopSection />
    </div>
  </div>
</template>

<script lang="ts" setup>
import Background from './components/Background.vue';
</script>

<style>
body {
  margin: 0;
  padding: 0;
  font-family: 'JetBrains Mono', sans-serif;
  background-color: black;
  color: white;
}

.sections {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  gap: 100vh;
  /* セクション間の間隔（画面いっぱいのスペースを確保） */
}

.section {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 80%;
  height: 100vh;
  margin: 0 auto;
  border-radius: 10px;
  color: white;
  opacity: 0;
  /* 初期状態は非表示 */
  transition: opacity 1s, transform 1s;
}

.section:first-child {
  opacity: 1 !important;
  /* フェードを無効化 */
}

.section.text-center {
  text-align: center;
}

</style>