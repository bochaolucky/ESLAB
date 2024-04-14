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
