<template name="component-name">
  <div>
    <p>{{ ip }}</p>
    <el-button type="primary" @click="getIp">Button</el-button>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      ip: '0.0.0.0'
    }
  },
  methods: {
    async getIp() {
      // await 同期待ち
      this.ip = await this.$axios.$get('http://icanhazip.com')
    }
  },
};
</script>

<style>
  div{
    text-align: center;
    line-height: 2;
    font-size: 32px;
  }
  .el-button{
    font-size: 24px;
  }
</style>
