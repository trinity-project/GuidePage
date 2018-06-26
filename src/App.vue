<template>
  <div id="app">
    <headNav/>
    <index/>
  </div>
</template>

<script>
import headNav from './components/headNav'
import index from './components/index'

export default {
  name: 'App',
  components: {
    headNav,index
  }
}
</script>

<style>
#app {
  /* font-family: 'Avenir', Helvetica, Arial, sans-serif; */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
html,body{
  margin: 0;
  padding: 0;
  background: RGBA(254, 252, 247, 1.00);
}
.el-menu--horizontal {
  padding: 8px 5px;
  width: 1400px;
  margin: 0 auto;
  border-bottom: solid 7px #e6e6e6;
}
</style>
