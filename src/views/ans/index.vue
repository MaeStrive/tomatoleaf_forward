<template>
  <div style="margin: 2.5%">
    <div style="text-align: center;font-size: 25px;color: rgba(1, 239, 183, 0.73)">番茄病害智能问答</div>
    <div style="text-align: center">
      <el-input v-model="question" placeholder="请输入问题" style="height: 60px"></el-input>
      <el-button type="success" @click="submitQuestion" style="margin-top: 2%" size="large">提交</el-button>
      <div style="height: 150px;border: 1px solid #bebcb8;padding-top: 2%;margin-top: 2%">{{ answer }}</div>
    </div>
  </div>
</template>
<script lang="ts" setup>
import {ref} from 'vue'
import axios from 'axios';

const question = ref()
const answer = ref()

async function submitQuestion() {
  try {
    const response = await axios.get('http://localhost:8000/login/', {
      params: {
        question: question.value
      },
    });
    // console.log(response.data)
    let data=response.data
    const parser = new DOMParser();
    const doc = parser.parseFromString(data, 'text/html');

// 现在您可以访问和操作获取的 DOM 对象
    const titleElement = doc.querySelector('.title');
    const titleData = titleElement.textContent;
    console.log(titleData);
    answer.value=titleData
  } catch (error) {
    alert(error)
  }
}
</script>
<style scoped>
.el-carousel__item h3 {
  color: #475669;
  opacity: 0.75;
  line-height: 200px;
  margin: 0;
  text-align: center;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}
</style>
