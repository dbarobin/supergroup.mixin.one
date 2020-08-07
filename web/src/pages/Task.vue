<template>
  <div class="wrapper">
    <h2>您需要使用一次「水龙头」才能加入「水龙头 App 中文群」</h2>
    <h3>
      搜索
      <span @click="showRobot">水龙头 App 机器人: 7000000014</span>，不花钱定投比特币。
    </h3>
    <h3>
      <a href="https://w3c.group/c/1590584538524446">点此查看操作流程</a>
    </h3>
  </div>
</template>

<script>
// import { Toast } from 'vant'

export default {
  data() {
    return {
      robotUuid: "1da1124a-9c97-4f2b-b332-f11f77c7604a"
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
  background: #ce0e2f;
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