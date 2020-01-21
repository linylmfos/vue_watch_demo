<template>
    <div id="root6">
      <h3>watch用法6： 监听对象属性</h3>
      <input type="text" v-model="deepMessage.a.b">
      <span>{{copyMessage}}</span>
    </div>
</template>


<script>
export default {
  name: 'WatchCom6',
  props: {
    msg: String
  },
  data() {
    return {
      deepMessage: { 
        a:{ 
          b: 'hello vue'
        } 
      },
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
    'deepMessage.a.b' : 'handleMessage'
  }
}
</script>
