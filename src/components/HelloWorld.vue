<template>
  <div class="hello">
    <!-- <div id="root">
      <h3>watch用法1： 常见用法</h3>
      <input type="text" v-model="message">
      <span>{{copyMessage}}</span>
    </div>
    
   
    <div id="root4">
      <h3>watch用法4： immediate</h3>
      <input type="text" v-model="message">
      <span>{{copyMessage}}</span>
    </div>
    <div id="root5"> 
      <h3>watch用法5： 绑定多个handler</h3>
      <input type="text" v-model="message">
      <span>{{copyMessage}}</span>
    </div>
    <div id="root6">
      <h3>watch用法6： 监听对象属性</h3>
      <input type="text" v-model="deepMessage.a.b">
      <span>{{copyMessage}}</span>
    </div> -->
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      message: 'hello vue',
      copyMessage: ''
    }
  }
}
</script>
