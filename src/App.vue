<template>
  <div id="app">
    <div>
       <el-button @click="openDiag = true" type="primary">Welcome</el-button>
       <el-dialog :visible.sync="openDiag">
       <input type="text" v-model="sendTreat"><HelloWorld msg="Welcome to Your Vue.js App"/>
       <Simba :treat="sendTreat"/>
       </el-dialog>
    </div>

  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Simba from './components/Simba.vue'
export default {
  name: 'app',
  components: {
    HelloWorld,
    Simba
  },
  data: function () {
    return {
      sendTreat:"kITTY SNACKS",
      openDiag: false
    }
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