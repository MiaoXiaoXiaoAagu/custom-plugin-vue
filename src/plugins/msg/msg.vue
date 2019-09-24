<template>
  <div>
    <div class="msg" :class="{active:msgStatus}">
        <div>{{text}}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'vue-msg',
  data () {
    return {
      msgStatus: false,
      text: ''
    }
  },
  methods: {
    msgPlugin (msg, time = 2000) {
      this.text = msg
      this.msgStatus = true
      setTimeout(() => {
        this.msgStatus = false
      }, 1000)
    }
  }
}
</script>

<style scoped>
  .msg{
   position: absolute;
   left: 50%;
    top: 30%;
    transform: translate(-50%,50%);
    width: 0;
    height: 0;
    text-align: center;
    background-color: black;
    color: white;
    transition: all 0.5s;
    border-radius: 5px;
    z-index: -1;
    opacity: 0;
  }
  .msg.active{
    width: 150px;
    height: 25px;
    opacity: 1;
    z-index: 1;
  }
</style>
