<template>
  <div></div>
</template>

<script>
import { Toast } from "vant";

export default {
  async mounted() {
    const code = this.$route.query.code;
    const returnTo = this.$route.query.return_to;
    try {
      let resp = await this.GLOBAL.api.account.authenticate(code);
      if (resp && resp.data && resp.data.authentication_token) {
        if (returnTo) {
          this.$router.push(returnTo);
          return;
        }
        this.$router.push("/");
      }
    } catch (err) {
      if (err && err.code == 21000) {
        console.log(err);
        this.$router.push("/task");
        return;
      }
      Toast("OAuth Failed");
    }
  }
};
</script>