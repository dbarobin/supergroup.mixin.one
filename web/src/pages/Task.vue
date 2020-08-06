<template>
  <div class="wrapper">
    <h2>ExinOne 余币宝 FCoin 事件沟通群</h2>
    <h3>
      您在余币宝暂时没有资产，不能加入本群，如果有任何问题，请联系客服。
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