<template>
    <div id="root3">
      <h3>watch用法3： deep + handler</h3>
      <input type="text" v-model="deepMessage.a.b">
      <span>{{copyMessage}}</span>
    </div>
</template>


<script>
export default {
  name: 'WatchCom3',
  props: {
    msg: String
  },
  data() {
    return {
      deepMessage: {
        a: {
          b: 'Deep Message'
        },
        copyMessage: ''
      }
    }
  },
  methods: {
    /* eslint-disable */
    handleDeepMessage(value) {
      this.copyMessage = value.a.b;
    }
  },
  watch: {
    deepMessage: {
      handler: 'handleDeepMessage',
      deep: true
    }
  }
}
</script>
