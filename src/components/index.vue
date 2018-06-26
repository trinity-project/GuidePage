<template>
  <el-row :gutter="50" class="ContentBox">
    <el-col :span="24" style="height:100%;">
      <el-col :span="2" style="height:100%;">
        <div class="footBox">
            <!-- <h2>Help</h2> -->
        </div>
      </el-col>
      <el-col v-for="(Guide,index) in GuidesList" :key="index" :xs="24" :sm="5" :md="5" :lg="5" :xl="5" style="height:100%;">
        <a :href="Guide.link" target="_blank">
          <div class="GuidesBox">
            <div class="GuideBoxImg">
              <img :src="Guide.img" alt="" width="100%">
            </div>
            <div class="GuideBoxTxt">
              <h2>{{ Guide.title }}</h2>
              <p>{{ Guide.content }}</p>
            </div>
          </div>
        </a>
      </el-col>
      <el-col :span="2" style="height:100%;">

      </el-col>
    </el-col>
  </el-row>
</template>

<script>
export default {
  name: 'index',
  data () {
    return {
      GuidesList:[
        {
          link:"https://www.baidu.com",
          img:"static/img/Wallet.jpeg",
          title:"Trnity Wallet",
          content:"The Trinity state channel wallet is used to transfer on chain the state channel and to realize the off chain transactions."
        },
        {
          link:"https://www.baidu.com",
          img:"static/img/TStore.jpg",
          title:"T Store",
          content:"Trinity Online Experience Store is designed to provide users with a practical experience of state channel payment functionality."
        },
        {
          link:"https://www.baidu.com",
          img:"static/img/Faucet.jpeg",
          title:"Faucet",
          content:"The TNC faucet is based on NEO TestNet, which is designed for that everyone can try to use TNC on NEO TestNet."
        },
        {
          link:"https://www.baidu.com",
          img:"static/img/NetworkExplorer.jpeg",
          title:"Network Explorer",
          content:"The Trinity state channel wallet is used to transfer on chain the state channel and to realize the off chain transactions."
        },
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.ContentBox{
  height: calc(100vh - 262px);
  width: 100%;
  margin:50px auto ;
}
.GuidesBox{
  width: 100%;
  height: 100%;
    padding: 20px;
  /* background: #CCC; */
  transition: 0.6s;
  cursor: pointer;
}
.GuidesBox:hover{
  transform:scale(1.02); 
  /* padding: 12px; */
  background: RGBA(240, 240, 240, 1.00)
}
.GuideBoxImg{
  height: 500px;
  /* max-height:600px; */
  width: 100%;
  /* background: #EEE; */
  overflow: hidden;
  display: table-cell;
  vertical-align: middle;
}
.GuideBoxImg img{
  /* position: absolute;
  top: 50%;
  margin-top: -25px; */
}
.GuideBoxTxt{
  height: 23%;
  width: 100%;
  /* background: #CCC; */
  text-align: center;
  overflow: hidden;
}
h2{
  font-size: 24px;
}
a{ 
  text-decoration:none; 
  color:#333; 
} 
.footBox{
  display: table-cell;
  vertical-align: middle;
  /* writing-mode: vertical-lr;
  transform: rotate(180deg);
  padding-bottom: 150%; */
}
</style>
