<template>

  <el-container direction="vertical">
    <myheader index="/"></myheader>

    <el-main class="main-content">
    
      <el-row :gutter="0" type="flex" justify="center">
        <el-col :xs="14" :sm="9" :md="8" :lg="14" :xl="14">
          <el-divider></el-divider>

          <h1>嵌入式系统研究组</h1>
          <p style="text-indent:2em">
            嵌入式研究组成立于202年，实验室研究方向为嵌入式系统，最近转向自动驾驶和实时机器人操作系统（ROS），以及无电池能量采集系统。在与我的研究合作伙伴的合作下，我们深入研究了操作系统和运行时、间歇计算和值得信赖的实时边缘人工智能，特别关注自动驾驶。

            研究组负责人刘松冉助理教授，于东北大学信息科学与工程学院，获学士和硕士学位，毕业于东北学院计算机科学与工程院，获博士学位，导师为王毅教授(王义) 和南关(关楠). 2020年至2021年间，香港理工大学计算机系的博士后研究员。
          </p>

          <el-divider><i class="el-icon-lock"></i></el-divider>

          <h1>研究方向</h1>

          <ul>主要研究兴趣在于嵌入式系统，最近转向自动驾驶和实时机器人操作系统（ROS），以及无电池能量采集系统。在与我的研究合作伙伴的合作下，我们深入研究了操作系统和运行时、间歇计算和值得信赖的实时边缘人工智能，特别关注自动驾驶。有关我们最近的努力，请访问ESL研究小组。
            <li>
              <h4>机器人操作系统</h4>
              <p>
                主要研究兴趣在于嵌入式系统，最近转向自动驾驶和实时机器人操作系统（ROS），以及无电池能量采集系统。在与我的研究合作伙伴的合作下，我们深入研究了操作系统和运行时、间歇计算和值得信赖的实时边缘人工智能，特别关注自动驾驶。有关我们最近的努力，请访问ESL研究小组。
              </p>
            </li>
          </ul>
          <h1>最新成果（这里目前不是咱们的成果）</h1>
          <h3 style="margin-top: 10px">FedCoin: A Peer-to-Peer Payment System for Federated Learning</h3>
   
          <p style="display: flex;align-items: center;margin-top: 10px">视频演示：</p>

          <div style="width: 100%;text-align: center">
            <video width="640" height="360" controls="controls" preload="metadata">
              <source :src="'/FedCoin.mp4'" type="video/mp4">
            </video>
          </div>

          <p style="display: flex;align-items: center;margin-top: 20px">备用播放地址1：
            <el-link href="https://v.youku.com/v_show/id_XNDU2NjA5NzQ3Mg==.html" target="_blank">优酷</el-link>
          </p>
          <p style="display: flex;align-items: center;margin-top: 10px">备用播放地址2：
            <el-link href="https://youtu.be/u5LPLdZvd0g" target="_blank">YouTube</el-link>
          </p>

        </el-col>
      </el-row>
    </el-main>


    <myfooter></myfooter>
  </el-container>
</template>

<script>
  import myheader from '~/components/myheader.vue'
  import myfooter from '~/components/myfooter.vue'

  export default {
    components: {
      myheader,
      myfooter
    }
  }
</script>

<style scoped>


  h4 {
    margin: 20px 0 10px 0;
  }

  p {
    line-height: 1.7;
    color: #606266;
  }


  .group-wrapper {
    height: 400px;
    width: 100%;
    margin: 10px auto;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
  }

  .group-bg {
    height: 100%;
    width: 100%;
    position: absolute;
    filter: blur(20px);
    transform: scale(1.1);
  }

  .group-ph {
    height: 400px;
    width: 800px;
  }


</style>
