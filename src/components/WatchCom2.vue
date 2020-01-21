<template>
   <div id="root2">
      <h3>watch用法2: 绑定方法</h3>
      <input type="text" v-model="message">
      <span>{{copyMessage}}</span>
    </div>
</template>


<script>
export default {
  name: 'WatchCom2',
  props: {
    msg: String
  },
  data() {
    return {
      message: 'hello vue',
      copyMessage: ''
    }
  },
  methods: {
    /* eslint-disable */
    handleMessage(value) {
      this.copyMessage = value
    }
  },
  watch: {
    message: 'handleMessage'
  }
}
</script>
