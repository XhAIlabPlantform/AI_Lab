<template>
  <body id="all"style="min-width: 13.6rem">
  <div id="header">
    <img src="../assets/控制台/banner.png">
  </div>
  <div id="body">
    <div id="aside">
      <sidebar></sidebar>
    </div>
    <div id="main">
      <div id="search">
        <p class="route"><router-link to="" class="linkto">控制台</router-link>&gt<router-link to="" class="linkto">功能</router-link>&gt人脸识别</p>
      </div>
      <div class="line">
        <div class="column">
          <div class="column_title">人脸检测</div>
          <div class="column_pic1"></div>
          <div class="column_word">检测图片中的人脸并标记出位置信息</div>
          <el-button class="button4submit">API文档</el-button>
        </div>
        <div class="column">
          <div class="column_title">人脸对比</div>
          <div class="column_pic2"></div>
          <div class="column_word">比对两张图片中人脸的相似度，并返回相似度分值</div>
          <el-button class="button4submit">API文档</el-button>
        </div>
      </div>
      <div class="line">
        <div class="column">
          <div class="column_title">人脸查找</div>
          <div class="column_pic3"></div>
          <div class="column_word">在指定人脸集合中，找出最相似的人脸</div>
          <el-button class="button4submit">API文档</el-button>
        </div>
      </div>
    </div>
  </div>
  </body>
</template>
<script>
  import sidebar from './SideBar.vue'
  export default {
    name:"ControllerFaceAPI",
    components: {sidebar},
    data() {
      return {
        isCollapse: true
      };
    },
    methods: {
      handleOpen(key, keyPath) {
        console.log(key, keyPath);
      },
      handleClose(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  }
</script>

<style scoped>
#find{
  width: 10%;
  height: 25%;
  margin: 0;
  position: relative;
  right:0.5%;
}
.linkto{
  color: #4096ff;
  text-decoration: none
}
#text{
  text-align: center;
  position: relative;

}
body,form,div,ul,ol,li,h1,h2,h3,h4,h5,h6,table,tr,th,td,p,input,dl,dt,dd,ul,ol,li,input,textarea { font-family:"微软雅黑"!important;}
textarea{
  overflow:auto;
  background: transparent;
  color: black;
  border: none;
  resize: none;
  font-weight:lighter;
  margin-bottom:0.3rem;
}
.line{
  width: 8.5rem;
  margin-left: 1rem;
  height: 3.5rem;
}

.column{
  float: left;
  width: 3.4rem !important;
  height: 4rem !important;
  margin-left:5% ;
  margin-right: 5%;
}

.column_title{
  width: 3.4rem;
  text-align: center;
  margin-bottom: 0.1rem;
}

.column_pic1{
  width: 3.4rem;
  height: 2.5rem;
  background-image: url("../assets/控制台/人脸识别/人脸检测.png") !important;
  background-position: center;
  background-size: 100% 100%;
}

.column_pic2{
  width: 3.4rem;
  height: 2.5rem;
  background-image: url("../assets/控制台/人脸识别/人脸对比.png") !important;
  background-position: center;
  background-size: 100% 100%;
}
.column_pic3{
  width: 3.4rem;
  height: 2.5rem;
  background-image: url("../assets/控制台/人脸识别/人脸查找.png") !important;
  background-position: center;
  background-size: 100% 100%;
}



.column_word{
  color: grey;
  font-size: 0.15rem;
  margin-top: 0.05rem;
  margin-bottom: 0.05rem;
}

/*.column_btn{*/
  /*width: 70%;*/
  /*margin-left: 15%;*/
  /*color: white;*/
  /*font-weight: 600;*/
  /*line-height: 0.5rem;*/
  /*background-color: blue;*/
/*}*/
.button4submit{
  color: white;
  background-color: #2285ea;
  height: 0.45rem;
  width: 2.0rem;
  font-size: 0.2rem;
}
.button4submit:hover{
  background-color: #2473d7;
  color: white;
}
.route{
  float: left;
  position: relative;
  top: 40%;
}
#search{
  height: 11%;
  padding-top:3%;
  padding-left: 5%;
  padding-bottom: 0;
}
.tac{
  height: 100%;
  width: 100%;
}
.teach{
  width: 100%;
  font-size: 0.15rem;
  margin-top: 0.1rem;
}
#main{
  float: left;
  height:100%;
  width: 74%;
  margin: 0;
  font-size: 0.21rem;
}
#aside{
  float: left;
  height: 15.3rem;
  width: 24%;
  margin: 0;
  box-shadow: 0 0.04rem 0.08rem 0 rgba(0, 0, 0, 0.2), 0 0.06rem 0.20rem 0 rgba(0, 0, 0, 0.10);
}
#body{
  height:73.42%;
  width: 100%;
  margin: 0;
}
img{
  height: 100%;
  width: 100%;
  margin: 0;
  padding: 0;
}
#header{
  height:5rem;
  width: 100%;
  background-color: black;
  margin: 0;
  padding: 0;
}
#all{
  height: 18rem;
  width: 100%;
  margin: 0;
  padding: 0;
}
#end{
  height: 2.47rem;
  width: 100%;
  margin: 0;
  padding: 0;
}
.from_group{
  display: flex;
  flex-direction: column;
  width: 74%;
  height: 12rem;
}
.blog{
  margin-top:0.4rem;
  margin-bottom:0.2rem;
  margin-left:0.820rem;
  width:7.92rem;
  height:2rem;
  box-shadow: 0 0.04rem 0.08rem 0 rgba(0, 0, 0, 0.2), 0 0.02rem 0.1rem 0 rgba(0, 0, 0, 0.1);
  cursor:default;
}
.bolg_title{
  margin-top:0.2rem;
  margin-bottom:0.1rem;
  margin-left:0.137rem;
  font-size:0.23rem;
  letter-spacing:0.03rem;
}
.icon{
  margin-right:0.164rem;
  height:0.133rem;
  width:0.133rem;
}
.outline{
  margin-top:0.2rem;
  margin-left:0.41rem;
  font-size:0.15rem;
  font-weight:900;
  color:  #303030;
  font-weight:450;
  line-height:0.267rem;
}
.more{
  margin-top:0.133rem;
  margin-left:0.41rem;
  font-size:0.15rem;
  color:#3399FF;
  letter-spacing:0.02rem;
  cursor:pointer;
}
.el-menu-vertical-demo{
  height:15rem;
}
span{
  font-size:0.22rem;
  margin-left: 0.6rem;
}

button{
  width: 1.20rem;
  height: 0.25rem;
  text-align: center;
  background: transparent;
  position: relative;
  border-width: 0.01rem;
  border-color: #4096ff;
  color:#4096ff;
  font-size: 0.15rem;
  cursor:pointer;
}
button:hover{
  background: white;
  border-width: 0.02rem;
  border-color: #4096ff;
}
button:active{
  background: #4096ff;
  border-color: transparent;
  color:white;
}

.searchInput{
  font-size:0.16rem;
  padding-left:0.137rem;
}
</style>
