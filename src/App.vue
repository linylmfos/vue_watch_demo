<template>
  <div id="app">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <watch-com></watch-com> 
    <watch-com2></watch-com2> 
    <watch-com3></watch-com3> 
    <watch-com4></watch-com4> 
    <watch-com5></watch-com5> 
    <watch-com6></watch-com6> 
    <hr>
    <class-style></class-style>
    <hr>
    <observable></observable>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import WatchCom from './components/WatchCom.vue'
import WatchCom2 from './components/WatchCom2.vue'
import WatchCom3 from './components/WatchCom3.vue'
import WatchCom4 from './components/WatchCom4.vue'
import WatchCom5 from './components/WatchCom5.vue'
import WatchCom6 from './components/WatchCom6.vue'
import ClassStyle from './components/styleclass/ClassStyle.vue';
import Observable from './components/Observable.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    WatchCom,
    WatchCom2,
    WatchCom3,
    WatchCom4,
    WatchCom5,
    WatchCom6,
    ClassStyle,
    Observable
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
