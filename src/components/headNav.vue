<template>
  <el-menu class="el-menu-demo navBox" mode="horizontal">
    <el-menu-item style="width: 10%;">

    </el-menu-item>
    <el-menu-item style="width: 80%;">
      <img src="./../assets/logo.png" alt="">
      <h1>{{ title }}</h1>
    </el-menu-item>
    <el-menu-item style="width: 10%;">
      <h2>Help</h2>
    </el-menu-item>
  </el-menu>
</template>

<script>
export default {
  name: 'headNav',
  data() {
  return {
      title:"Trinity State Channel Experience Guide Page"
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.navBox{
  width: 100%;
  max-width: 1300px;
  margin: 0 auto;
  background: RGBA(254, 252, 247, 1.00);
}
.el-menu-item img{
  width: 57px;
}

.el-menu--horizontal>.el-menu-item{
  text-align: center;
  cursor: default;
}
.el-menu--horizontal>.el-menu-item:hover{
  color:#909399;
}
.el-menu--horizontal>.el-menu-item.is-active{
  border-bottom:none;
  color:#909399;
}
.el-menu--horizontal .el-menu-item:not(.is-disabled):focus, .el-menu--horizontal .el-menu-item:not(.is-disabled):hover {
  background: RGBA(254, 252, 247, 1.00);
  color:#909399;
}
h1{
  display: inline;
}
h2{
  margin: 0;
  cursor: pointer;
}
</style>
