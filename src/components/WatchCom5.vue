<template>
    <div id="root5"> 
      <h3>watch用法5： 绑定多个handler</h3>
      <input type="text" v-model="message">
      <span>{{copyMessage}}</span>
    </div>
</template>


<script>
export default {
  name: 'WatchCom5',
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
    },
    handleMessage2(value) {
      this.copyMessage = this.copyMessage + '*'
    }
  },
  watch: {
    message: [{
      handler: 'handleMessage'
    },
    'handleMessage2', function(value) {
      this.copyMessage = this.copyMessage + '...';
    } 
    ]
  }
}
</script>
