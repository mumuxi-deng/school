<template>
  <div>
    <header>
      <div class="heard"></div>
    </header>
    <article class="article">
      <div>
        <img src="https://www.gdust.edu.cn//e/images/s1/logo11.png" alt="" />
      </div>
      <div class="naveMun">
        <el-menu
          class="el-menu-demo"
          text-color="white"
          background-color="#004da0"
          mode="horizontal"
        >
          <el-menu-item index="1">学校首页</el-menu-item>
          <el-submenu index="2">
            <template slot="title">我的工作台</template>
            <el-menu-item index="2-1">选项1</el-menu-item>
            <el-menu-item index="2-2">选项2</el-menu-item>
            <el-menu-item index="2-3">选项3</el-menu-item>
            <el-submenu index="2-4">
              <template slot="title">选项4</template>
              <el-menu-item index="2-4-1">选项1</el-menu-item>
              <el-menu-item index="2-4-2">选项2</el-menu-item>
              <el-menu-item index="2-4-3">选项3</el-menu-item>
            </el-submenu>
          </el-submenu>
          <el-menu-item index="3" disabled>消息中心</el-menu-item>
          <el-menu-item index="4">
            <a href="https://www.ele.me" target="_blank">订单管理</a>
          </el-menu-item>
        </el-menu>
        <el-dropdown>
          <el-button type="primary">
            更多菜单<i class="el-icon-arrow-down el-icon--right"></i>
          </el-button>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>黄金糕灌灌灌灌灌</el-dropdown-item>
            <el-dropdown-item>狮子头g'g'g'g</el-dropdown-item>
            <el-dropdown-item>螺蛳灌灌灌灌灌粉</el-dropdown-item>
            <el-dropdown-item>双皮灌灌灌灌奶</el-dropdown-item>
            <el-dropdown-item>蚵仔灌灌灌灌煎</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
      </div>
      <div v-for="(item, index) in news" :key="index">
        <news :news="item"></news>
      </div>
    </article>
  </div>
</template>

<script>
import news from "../components/news";
export default {
  data() {
    return {
      news: [
        {
          title: "学校要闻",
          more: "更多",
          content: ["教案设计速度发了就爱上。", "jsj金卡健身房锻炼静安寺"],
        },
        {
          title: "学校要闻",
          more: "更多",
          content: ["教案设计速度发了就爱上。", "jsj金卡健身房锻炼静安寺"],
        },
      ],
    };
  },
  components: { news },
  created() {
    console.log(this.news);
  },
};
</script>

<style>
.heard {
  height: 30px;
  background: #004da0;
}
.article {
  width: 1200px;
  margin: auto;
}
.naveMun {
  height: 40px;
  background: #004da0;
}
</style>