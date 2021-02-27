<template>
  <div class="hello">
    <div>
      <el-row>
        <el-col :span="12"
          ><div class="grid-content bg-purple">{{ news.title }}</div></el-col
        >
        <el-col :span="12" v-if="news.more"
          ><div class="grid-content bg-purple-light">
            {{ news.more }}
          </div></el-col
        >
      </el-row>
    </div>
    <el-divider></el-divider>
    <p v-for="(item, index) in news.content" :key="index">
      {{ item }}
    </p>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
    };
  },
  props: ["news"],
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
