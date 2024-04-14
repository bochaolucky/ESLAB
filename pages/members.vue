<template>
  <el-container direction="vertical">
    <myheader index="/members"></myheader>
    <el-main class="main-content">
      <el-row :gutter="0" type="flex" justify="center">
        <el-col :span="4" style="min-width: 240px">
          <div
            style="position: fixed;display: flex;justify-content: center;align-items:center;width: 200px;height: 500px">

            <ul class="ul-navi">
              <li :class="{active: active===0}" @click="scrollTo('#h1-teacher')">实验室负责人</li>
              <li :class="{active: active===1}" @click="scrollTo('#h1-master-2021')">2021级硕士研究生</li>
              <li :class="{active: active===1}" @click="scrollTo('#h1-master-2021')">2022级硕士研究生</li>
              <li :class="{active: active===1}" @click="scrollTo('#h1-master-2023')">2023级硕士研究生</li>
              <li :class="{active: active===1}" @click="scrollTo('#h1-master-2023')">2024级硕士研究生</li>
            </ul>

          </div>
        </el-col>


        <el-col :xs="18" :sm="16" :md="14" :lg="12" :xl="10"
                style="display: flex;justify-content: center;flex-wrap: wrap;" class="wrapper">

          
          <head>
          <meta charset="UTF-8">
          <title>区域点击跳转示例</title>
          <style>
            /* 移除链接的默认样式 */
            a {
              text-decoration: none; /* 移除下划线 */
              color: inherit; /* 继承父元素的字体颜色 */
            }

            /* 自定义链接覆盖的区域样式 */
            .link-area {
              background-color: #f0f0f0; /* 背景颜色 */
              padding: 50px; /* 内边距 */
              border: 10px solid #ddd; /* 边框 */
              margin-left: 50px;
              width: 500px;
              display: inline-block; /* 使 div 可点击 */
              cursor: pointer; /* 鼠标悬停时显示手形光标 */
            }
          </style>
          </head>
          <body>
          <h1 id="h1-teacher">实验室负责人</h1>
          <a href="https://liusongran.github.io/" target="_blank">
          <member
            name="刘松冉"
            avatar="/avatar/liusongran.png"
            letter="L"
            position="特聘助理教授"
            email="liusongran@neu.edu.cn"
            description="毕业于东北大学信息科学与工程学院，获学士和硕士学位，毕业于东北学院计算机科学与工程院，获博士学位，导师为王义教授和关楠. 2020年至2021年间，香港理工大学计算机系的博士后研究员。"
            href="https://liusongran.github.io/"
          > <a href="https://www.example.com">点击这里访问Example网站></a>
          </member>
          </a
          <el-divider></el-divider>


          <h1 id="h1-master-2021">2021级硕士研究生</h1>
          <member
            name="王子龙"
            avatar="/avatar/wangzilong.png"
            letter="L"
            position="2021级硕士研究生"
            email="zilong.com"
            description="2021年毕业于河北大学，获学士学位。现就读于东北大学计算机科学与技术专业，导师是刘松冉特聘助理教授。"
            
          ></member>

          <el-divider></el-divider>


          <h1 id="h1-master-2022">2022级硕士研究生</h1>
          <member
            name="孙博瀚"
            avatar="/avatar/bohan.jpg"
            letter="L"
            position="2023级硕士研究生"
            email="bohan@qq.com"
            description="2022年毕业于合肥工业大学，获学士学位。现就读于东北大学计算机科学与技术专业，导师是刘松冉特聘助理教授。"
          ></member>

          <el-divider></el-divider>


          <h1 id="h1-master-2023">2023级硕士研究生</h1>
          <member
            name="曹博超"
            avatar="/avatar/曹博超.jpg"
            letter="L"
            position="2023级硕士研究生"
            email="583238141@qq.com"
            description="2023年毕业于燕山大学，获计算机科学与技术学士学位。现就读于东北大学计算机科学与技术专业，导师是刘松冉与唐月特聘助理教授。"
          ></member>

           <member
            name="陈静波"
            avatar="/avatar/chenjingbo.jpg"
            letter="L"
            position="2023级硕士研究生"
            email="jingbo@qq.com"
            description="2023年于上海师范大学天华学院，获计算机科学与技术学士学位。现就读于东北大学计算机科学与技术专业，导师是刘松冉特聘助理教授。"
          ></member>
           <h1 id="h1-master-2022">2024级硕士研究生</h1>
          <member
            name="徐家福"
            avatar="/avatar/jiafu.jpg"
            letter="L"
            position="2023级硕士研究生"
            email="FAIZ030612@163.com"
            description="目前就读于河北大学计算机科学与技术专业，已推免至东北大学智慧系统实验室嵌入式研究组"
          ></member>
          </body>
        </el-col>
      </el-row>
    </el-main>
    <myfooter></myfooter>
  </el-container>
</template>

<script>
  import myheader from '~/components/myheader.vue'
  import myfooter from '~/components/myfooter.vue'
  import Member from "../components/member.vue";

  export default {
    name: "members",
    components: {
      Member,
      myheader,
      myfooter
    },
    data() {
      return {
        active: 0
      }
    },
    mounted() {
      window.addEventListener('scroll', this.onScroll)
    },
    destroyed() {
      window.removeEventListener('scroll', this.onScroll)
    },
    methods: {
      onScroll() {
        // 获取所有锚点元素
        const navContents = document.querySelectorAll('.wrapper h1');
        // 所有锚点元素的 offsetTop
        const offsetTopArr = [];
        navContents.forEach(item => {
          offsetTopArr.push(item.offsetTop)
        });
        // 获取当前文档流的 scrollTop
        const scrollTop = document.documentElement.scrollTop || document.body.scrollTop;
        // 定义当前点亮的导航下标
        let navIndex = 0;
        for (let n = 0; n < offsetTopArr.length; n++) {
          // 如果 scrollTop 大于等于第 n 个元素的 offsetTop 则说明 n-1 的内容已经完全不可见
          // 那么此时导航索引就应该是 n 了
          if (scrollTop >= offsetTopArr[n]) {
            navIndex = n
          }
        }
        // 把下标赋值给 vue 的 data
        this.active = navIndex
      },
      // 跳转到指定索引的元素
      scrollTo(content_id) {
        // 获取目标的 offsetTop
        // css选择器是从 1 开始计数，我们是从 0 开始，所以要 +1

        const targetOffsetTop = document.querySelector(content_id).offsetTop
        // 获取当前 offsetTop
        let scrollTop = document.documentElement.scrollTop || document.body.scrollTop
        // 定义一次跳 50 个像素，数字越大跳得越快，但是会有掉帧得感觉
        const STEP = 50
        // 判断是往下滑还是往上滑
        if (scrollTop > targetOffsetTop) {
          // 往上滑
          smoothUp()
        } else {
          // 往下滑
          smoothDown()
        }

        // 定义往下滑函数
        function smoothDown() {
          // 如果当前 scrollTop 小于 targetOffsetTop 说明视口还没滑到指定位置
          if (scrollTop < targetOffsetTop) {
            // 如果和目标相差距离大于等于 STEP 就跳 STEP
            // 否则直接跳到目标点，目标是为了防止跳过了。
            if (targetOffsetTop - scrollTop >= STEP) {
              scrollTop += STEP
            } else {
              scrollTop = targetOffsetTop
            }
            document.body.scrollTop = scrollTop
            document.documentElement.scrollTop = scrollTop
            // 屏幕在绘制下一帧时会回调传给 requestAnimationFrame 的函数
            // 关于 requestAnimationFrame 可以自己查一下，在这种场景下，相比 setInterval 性价比更高
            requestAnimationFrame(smoothDown)
          }
        }

        // 定义往上滑函数
        function smoothUp() {
          if (scrollTop > targetOffsetTop) {
            if (scrollTop - targetOffsetTop >= STEP) {
              scrollTop -= STEP
            } else {
              scrollTop = targetOffsetTop
            }
            document.body.scrollTop = scrollTop
            document.documentElement.scrollTop = scrollTop
            requestAnimationFrame(smoothUp)
          }
        }
      }

    }
  }
</script>

<style scoped>

  h1 {
    width: 100%;
  }

  .ul-navi {
    font-size: 1.3rem;
    font-weight: bold;
    color: #909399;
    width: 100%;
  }

  .ul-navi li {
    cursor: pointer;
    margin: 30px 0;
  }

  .ul-navi .active {
    font-size: 1.5rem;
    color: #303133;
  }
</style>
