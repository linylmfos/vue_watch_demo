<template>
    <div id="root4">
      <h3>watch用法4： immediate</h3>
      <input type="text" v-model="message">
      <span>{{copyMessage}}</span>
    </div>
</template>


<script>
export default {
  name: 'WatchCom4',
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
      this.copyMessage = value;  
    }
  },
  watch: {
    message: {
      handler: 'handleMessage',
      immediate: true
    }
  }
}
</script>
