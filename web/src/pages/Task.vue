<template>
  <div class="wrapper">
    <h2> 抱歉，您暂时不是蓝盾用户，暂无法加入 </h2>
    <h3>
      搜索
      <span @click="showRobot"> 机器人 ID: 7000000015</span>，ExinLocal 是一个全球买卖加密货币的去中心化点对点市场。。
    </h3>
    <h3>
      <a href="https://support.exinlocal.com/#/zh-cn/trust">点此查看文档</a>
      <a href="https://hk.exinlocal.com/#/mine/applyCertification">点此申请蓝盾</a>
    </h3>
  </div>
</template>

<script>
// import { Toast } from 'vant'
export default {
  data() {
    return {
      robotUuid: "f2397b7a-ddfc-4bd9-925a-e14a9a553ba5"
    };
  },
  methods: {
    showRobot() {
      window.location.href = `mixin://users/${this.robotUuid}`;
    }
  }
};
</script>

<style scoped>
.wrapper {
  background: #00b9a6;
  padding: 5vw;
  color: white;
  height: 100%;
}
.wrapper a {
  color: white;
  text-decoration: underline;
}
.wrapper span {
  text-decoration: underline;
}
</style>