<template>

  <el-container direction="vertical">
    <myheader index="/"></myheader>

    <el-main class="main-content">
      <el-row :gutter="0" type="flex" justify="center">
        <el-col :xs="20" :sm="18" :md="16" :lg="14" :xl="14">

          <div class="group-wrapper animated bounceInDown">
            <el-image class="group-bg" fit="fill" src="/group.jpg"></el-image>
            <el-image class="group-ph" src="/group.jpg"></el-image>
          </div>

          <el-divider></el-divider>

          <h1>嵌入式研究组</h1>
          <p style="text-indent:2em">
            实验室成立于2017年，目前实验室的leader为刘松冉特聘助理教授。其于东北大学信息科学与工程学院，获学士和硕士学位，毕业于东北学院计算机科学与工程院，获博士学位，导师为王毅教授(王义) 和南关(关楠). 2020年至2021年间，为香港理工大学计算机系的博士后研究员。
            其研究兴趣在于嵌入式系统，最近转向自动驾驶和实时机器人操作系统（ROS），以及无电池能量采集系统。在与我的研究合作伙伴的合作下，我们深入研究了操作系统和运行时、间歇计算和值得信赖的实时边缘人工智能，特别关注自动驾驶。有关我们最近的努力，请访问ESL研究小组。
          </p>


          <el-divider><i class="el-icon-lock"></i></el-divider>

          <h1>研究方向</h1>

          <ul>
            <li>
              <h4>机器人操作系统</h4>
              <p>
               最近转向自动驾驶和实时机器人操作系统（ROS），以及无电池能量采集系统。在与我的研究合作伙伴的合作下，我们深入研究了操作系统和运行时、间歇计算和值得信赖的实时边缘人工智能，特别关注自动驾驶。有关我们最近的努力，请访问ESL研究小组。
              </p>

              <h4>机器人操作系统</h4>
              <p>
               最近转向自动驾驶和实时机器人操作系统（ROS），以及无电池能量采集系统。在与我的研究合作伙伴的合作下，我们深入研究了操作系统和运行时、间歇计算和值得信赖的实时边缘人工智能，特别关注自动驾驶。有关我们最近的努力，请访问ESL研究小组。
              </p>

              <h4>机器人操作系统</h4>
              <p>
               最近转向自动驾驶和实时机器人操作系统（ROS），以及无电池能量采集系统。在与我的研究合作伙伴的合作下，我们深入研究了操作系统和运行时、间歇计算和值得信赖的实时边缘人工智能，特别关注自动驾驶。有关我们最近的努力，请访问ESL研究小组。
              </p>
            </li>

          </ul>

          <h1>科研项目</h1>
          <ul>
            <li>
              <h4>Intermittent Computing Systems（视频啥的以后换成咱们自己的）</h4>
              <p>
               最近转向自动驾驶和实时机器人操作系统（ROS），以及无电池能量采集系统。在与我的研究合作伙伴的合作下，我们深入研究了操作系统和运行时、间歇计算和值得信赖的实时边缘人工智能，特别关注自动驾驶。有关我们最近的努力，请访问ESL研究小组。（内容与实际无关）
              </p>

                  <p style="display: flex;align-items: center;margin-top: 20px">查看论文：
                    <el-link href="https://arxiv.org/abs/2002.11711" target="_blank">https://arxiv.org/abs/2002.11711</el-link>
                  </p>
                  <p style="display: flex;align-items: center;margin-top: 10px">在线实验：
                    <el-link href="http://demo.blockchain-neu.com" target="_blank">http://demo.blockchain-neu.com</el-link>
                  </p>

                  <p style="display: flex;align-items: center;margin-top: 10px">视频演示：</p>

                  <div style="width: 100%;text-align: center">
                    <video width="640" height="360" controls="controls" preload="metadata">
                    <source :src="'/FedCoin.mp4'" type="video/mp4">
                    </video>
                  </div>

                  <p style="display: flex;align-items: center;margin-top: 20px">备用播放地址1（以后换成咱们自己的）：
                    <el-link href="https://v.youku.com/v_show/id_XNDU2NjA5NzQ3Mg==.html" target="_blank">优酷</el-link>
                  </p>
                    <p style="display: flex;align-items: center;margin-top: 10px">备用播放地址2：
                    <el-link href="https://youtu.be/u5LPLdZvd0g" target="_blank">YouTube</el-link>
                  </p>

                  <br>
            </li>

          </ul>

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
