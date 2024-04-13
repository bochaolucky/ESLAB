<template>
  <el-container direction="vertical">
    <myheader index="/achievements"></myheader>
    <el-main class="main-content">

      <el-row :gutter="0" type="flex" justify="center">
        <el-col :xs="20" :sm="18" :md="16" :lg="14" :xl="12">
          <el-divider></el-divider>
          <el-divider><i class="el-icon-notebook-2"></i></el-divider>

          <h1>发表论文</h1>

          <h3>2024</h3>

          <ul>
            <li v-for="item in papers2024" class="item animated zoomIn">
              {{item}}
            </li>
          </ul>

          <h3>2023</h3>

          <ul>
            <li v-for="item in papers2023" class="item animated zoomIn">
              {{item}}
            </li>
          </ul>
          <h3>2022</h3>

          <ul>
            <li v-for="item in papers2022" class="item animated zoomIn">
              {{item}}
            </li>
          </ul>
        <h3>2021</h3>

          <ul>
            <li v-for="item in papers2021" class="item animated zoomIn">
              {{item}}
            </li>
          </ul>
        <h3>2020</h3>

          <ul>
            <li v-for="item in papers2020" class="item animated zoomIn">
              {{item}}
            </li>
          </ul>
                                                    

          </ul>

                   <el-divider><i class="el-icon-copy-document"></i></el-divider>

          <h1>获得奖项</h1>

          <ul>
            <li v-for="item in awards" class="item">
              {{item}}
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
    name: "achievements",
    data() {
      return {
        papers2024: [
          'RTeX: an Efficient and Timing-Predictable Multi-threaded Executor for ROS 2. Songrna Liu, Xu Jiang, Nan Guan, Zilong Wang, Minghe Yu and Yi Wang. IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems, 2024 CCF A类' 
        ],
        papers2023: [
          'Light Flash Write for Efficient Firmware Update on Energy-harvesting IoT Devices. Songran Liu, Mingsong Lv, Wei Zhang, Nan Guan. Design, Automation and Test in Europe (DATE), 2023 Best paper nomination!CCF B类',
          'Optimizing End-to-End Latency of Sporadic Cause-Effect Chains Using Priority Inheritance. Yue Tang, Xu Jiang, Nan Guan, Songran Liu, Xiantong Luo and Yi Wang. IEEE Real-Time Systems Symposium (RTSS), 2023 CCF A类',
          'Modeling and Analysis of Inter-Process Communication Delay in ROS 2. Xiantong Luo, Xu Jiang, Nan Guan, Haochun Liang, Songran Liu and Wang Yi. IEEE Real-Time Systems Symposium (RTSS), 2023 CCF A类',
        ],
        papers2022: [
          'Adaptive Task-based Intermittent Computing System with Parallel State Backup. Wei Zhang, Mingsong Lv, Songran Liu, Nan Guan. IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems (TCAD), 2022 CCF A类',
        ],
        papers2021: [
          'LATICS: A low-overhead adaptive task-based intermittent computing system. Songran Liu, Mingsong Lv, Wei Zhang, Nan Guan. IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems (TCAD), 2021 CCF A类',
         'Surviving Transient Power Failures with SRAM Data Retention. Songran Liu, Mingsong Lv, Wei Zhang, Nan Guan. Design, Automation and Test in Europe (DATE), 2021 CCF B类',
         'Intermittent Computing with Efﬁcient State Backup by Asynchronous DMA. Wei Zhang, Songran Liu, Mingsong Lv, Nan Guan. Design, Automation and Test in Europe (DATE), 2021 CCF B类',
        ],
        papers2020: [
          'Leaking your engine speed by spectrum analysis of real-Time scheduling sequences. Songran Liu, Nan Guan, Dong Ji, Weichen Liu, Xue Liu, Wang Yi. Journal of Systems Architecture, 2019 CCF B类',
          'MiniTEE—A Lightweight TrustZone-Assisted TEE for Real-Time Systems. Songran Liu, Nan Guan, Zhishan Guo, Wang Yi. Electronics, 2020',
        ],
        awards: [
          'Best paper nomination award, Light Flash Write for Efficient Firmware Update on Energy-harvesting IoT Devices, DATE23',
        ]
      }
    },
    components: {
      myheader,
      myfooter
    }
  }
</script>

<style scoped>

  .item {
    margin: 10px 0;
  }


  li {
    color: #606266;
    text-align: justify;
    text-justify: inter-ideograph
  }


</style>


