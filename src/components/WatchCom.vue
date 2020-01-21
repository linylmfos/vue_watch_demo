<template>
    <div id="root">
      <h3>watch用法1： 常见用法</h3>
      <input type="text" v-model="message">
      <span>{{copyMessage}}</span>
    </div>
</template>


<script>
export default {
  name: 'WatchCom',
  props: {
    msg: String
  },
  data() {
    return {
      message: 'hello vue',
      copyMessage: ''
    }
  },
  watch: {
    message(value) {
      this.copyMessage = value;
    }
  }
}
</script>
