<template>
  <div >
    <h1>hellow</h1>
    <input placeholder="请输入姓名" v-model="name">
    <button @click="submit">提交</button>
    <vue-msg ref="msgDom"></vue-msg>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      name: ''
    }
  },
  methods: {
    submit () {
      this.$refs.msgDom.msgPlugin('姓名不能为空')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
