<template>
  <el-container direction="vertical">
    <myheader index="/friends"></myheader>
    <el-main class="main-content">
      <el-row :gutter="0" type="flex" justify="center">
        <el-col :xs="20" :sm="18" :md="16" :lg="14" :xl="12">
          <h1>常用链接</h1>
          <div style="padding: 10px">
            <ul>
              <li> <el-link href="https://www.ccf.org.cn/ccf/contentcore/resource/download?ID=144845" target="_blank">中国计算机学会推荐国际学术会议和期刊目录 - 2019</el-link></li>
              <li> <el-link href="http://www.fenqubiao.com" target="_blank">中国科学院文献情报中心期刊分区表</el-link></li>
              <li> <el-link href="http://www.letpub.com.cn/index.php?page=grant" target="_blank">国家自然基金项目查询</el-link></li>
              <li> <el-link href="http://faculty.neu.edu.cn/sites.htm" target="_blank">东北大学教师列表</el-link></li>
              <li> <el-link href="http://www.neu.edu.cn/2019/0220/c175a237/page.htm" target="_blank">东北大学校历查询</el-link></li>
            </ul>
          </div>
          <h1>合作交流</h1>
          <div style="padding: 10px">
            <ul>
              <li> <el-link href="http://faculty.neu.edu.cn/tangyue/en/index.htm" target="_blank">Tang Yue</el-link></li>

            </ul>
          </div>
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
    name: "friends",
    components: {
      myheader,
      myfooter
    }
  }
</script>

<style scoped>

  li{
    font-size: 1.3rem;
    line-height: 1.7;
  }

  a{
    text-decoration: none;
  }
</style>
