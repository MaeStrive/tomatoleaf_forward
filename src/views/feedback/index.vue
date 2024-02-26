<template>
  <div style="margin: 2.5%">
    <div style="text-align: center; font-size: 25px; color: rgba(1, 239, 183, 0.73)">反馈</div>
    <div style="text-align: center; margin-top: 1.5%">
      <div>请留下您宝贵的意见!</div>
      <el-input v-model="question" placeholder="请输入问题" style="height: 60px" />
      <el-button type="success" @click="submitQuestion" style="margin-top: 2%" size="large">提交</el-button>
    </div>
  </div>
</template>
<script lang="ts" setup></script>
<style scoped>
.el-carousel__item h3 {
  color: #475669;
  opacity: 0.75;
  line-height: 200px;
  margin: 0;
  text-align: center;
}
</style>
