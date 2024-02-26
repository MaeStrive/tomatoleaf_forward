<template>
  <div style="margin: 2.5%">
    <div style="text-align: center; font-size: 25px; color: rgba(1, 239, 183, 0.73)">项目源码</div>
    <div style="text-align: center; margin-top: 2%">
      <div style="margin-top: 2%">
        <span style="padding-right: 2%; color: #1b8bfa; font-family: 楷体; font-size: large"
          >&emsp;&emsp;&emsp;YOLOv5</span
        ><el-button round type="success" @click="download('v5')">源码下载</el-button>
      </div>
      <div style="margin-top: 2%">
        <span style="padding-right: 2%; color: #1b8bfa; font-family: 楷体; font-size: large"
          >&emsp;&emsp;&emsp;YOLOv7</span
        ><el-button round type="success" @click="download('v7')">源码下载</el-button>
      </div>
      <div style="margin-top: 2%">
        <span style="padding-right: 2%; color: #1b8bfa; font-family: 楷体; font-size: large"
          >&emsp;&emsp;&emsp;YOLOv8</span
        ><el-button round type="success" @click="download('v8')">源码下载</el-button>
      </div>
      <div style="margin-top: 2%">
        <span style="padding-right: 2%; color: #1b8bfa; font-family: 楷体; font-size: large">Faster R-CNN</span
        ><el-button round type="success" @click="download('R-CNN')">源码下载</el-button>
      </div>
      <div style="margin-top: 2%">
        <span style="padding-right: 2%; color: #1b8bfa; font-family: 楷体; font-size: large"
          >&emsp;&emsp;&emsp;&emsp;&nbsp;SSD</span
        ><el-button round type="success" @click="download('SSD')">源码下载</el-button>
      </div>
      <div style="margin-top: 2%">
        <span style="padding-right: 2%; color: #1b8bfa; font-family: 楷体; font-size: large">bert智能问答</span>
        <el-button round type="success" @click="download('bert')">源码下载</el-button>
      </div>
    </div>
  </div>
</template>
<script lang="ts" setup>
async function download(info) {
  switch (info) {
    case "v5": {
      window.open("https://github.com/ultralytics/yolov5/archive/refs/heads/master.zip", "_blank")
      break
    }
    case "v7": {
      window.open("https://github.com/WongKinYiu/yolov7/archive/refs/heads/main.zip", "_blank")
      break
    }
    case "v8": {
      window.open("https://github.com/ultralytics/ultralytics/archive/refs/heads/main.zip", "_blank")
      break
    }
    case "R-CNN": {
      window.open("https://github.com/rbgirshick/py-faster-rcnn/archive/refs/heads/master.zip", "_blank")
      break
    }
    case "SSD": {
      window.open("https://github.com/amdegroot/ssd.pytorch/archive/refs/heads/master.zip", "_blank")
      break
    }
    case "bert": {
      window.open("https://github.com/google-research/bert/archive/refs/heads/master.zip", "_blank")
      break
    }
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
