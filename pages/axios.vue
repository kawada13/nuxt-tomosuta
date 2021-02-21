<template>
  <div style="padding: 30px">
    <el-button @click="fetchSomething">IPアドレスを取得</el-button>
    <p>{{ ip }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      ip:'aaa'
    }
  },
  methods: {
  async fetchSomething() {
    this.ip = await this.$axios.$get('http://icanhazip.com')
  },
}

}
</script>

<style>

</style>