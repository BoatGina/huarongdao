<template>
  <div id="app">
    <div class="container">

    </div>

    <div class="handle">
      <button>打乱顺序</button>
      <button>自动排好</button>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import Role from './components/Role.vue'

export default {
  name: 'app',

  data () {
    return {
      positions: {

      }
    }
  },

  components: {
    Role
  },

  methods: {
     async getResult () {
       const rs = await axios.post('http://ydtest.wps.cn/hrd/', this.positions)
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
  display:flex;
  justify-content: center;
  align-items: center; 
}
</style>
