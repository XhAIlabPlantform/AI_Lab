<!--这里是-->
<!--身份证识别分页面-->

<template>
  <div style="min-width: 13.6rem">
    <div id="AIhead" class="firstBackground">
      <div style="height: 1.50rem;"></div>
      <div class="table4this" style="margin-left: 20%">
        <tr style="font-size: 0.60rem;letter-spacing: 0.06rem;color:white;">身份证识别</tr>
        <div style="height: 0.20rem;"></div>
        <tr style="font-size: 0.22rem;color:white;">识别身份证正反面的文字信息</tr>
        <tr style="font-size: 0.22rem;color:white;"> </tr>
        <div style="height: 0.20rem;"></div>
        <tr><router-link to="/WordAPI"><el-button class="button4doc">技术文档</el-button></router-link></tr>
      </div>
    </div>
    <div id="AIbodyfir">
      <a id="introduce">功能介绍</a><br/>
      <a id="introducecontent">支持对二代居民身份证正反面的关键字段识别，包括姓名，性别，民族，出生日期，住址，身份证号，签发机关，有效日期。</a>
    </div>
    <div id="AIbodysec"class="secondBackground">
      <!--<img src="../assets/情感倾向分析/功能介绍.png"class="background">-->
      <button class="functionButton" id="apply"@click="VerifyAcc">接口申请</button>
      <button class="functionButton" id="download"@click="VerifyAcc2">SDK下载</button>
    </div>
    <div id="AIbodythi">
      <p id="txtApp">应用场景</p>
      <div class="card4this" style="width: 100%;">
        <div style="margin-right: auto;margin-left: 2.45rem;margin-top:0.50rem;width: 60%">
          <el-row :gutter="550" style="width: 13rem">
            <el-col :span="6"><div class="grid-content bg-purple">
              <el-card style="width: 3.36rem;height: 4rem;margin-right: 2rem" :body-style="{padding:'0rem'}">
                <div class="card4footer">
                </div>
                <div>
                  <div class="title4card">
                    <span>视频主播身份认证</span>
                  </div>
                  <div class="content4card">
                    <p style="font-size: 0.16rem;font-weight: 330">在视频直播场景，应用身份证OCR实现主播实名身份证识别和认证，减少人工录入成本，提高用户体验</p>
                  </div>
                </div>
              </el-card> </div></el-col>
            <el-col :span="10"><div class="grid-content bg-purple"><el-card style="width: 3.36rem;height: 4rem" :body-style="{padding:'0rem'}">
              <div class="card4footer2">
              </div>
              <div class="title4card">
                <span>远程身份认证</span>
              </div>
              <div class="content4card">
                <p style="font-size: 0.16rem;font-weight: 330">使用身份证，银行卡识别，以此实现用户信息的录入，应用于金融场景的用户身份认证，速度快，准确率高，减少用户输入成本，有效提高用户的体验</p>
              </div>
            </el-card></div></el-col>

          </el-row>
        </div>
      </div>

    </div>


    <!--  <img src="../assets/情感倾向分析/口碑分析.png" id="AIcar">
      <img src="../assets/情感倾向分析/舆情监控.png" id="AIcustomer"><br/>
      <textarea rows="1" cols="40" id="serviceCaption" disabled>视频主播身份认证</textarea>
      <textarea rows="1" cols="40" id="carCaption"disabled>远程身份认证</textarea><br/>
      <textarea rows="5" cols="40" id="serviceContent" disabled>在视频直播场景，应用身份证OCR实现主播实名身份证识别和认证，减少人工录入成本，提高用户体验</textarea>
      <textarea rows="5" cols="40" id="carContent" disabled>使用身份证，银行卡识别，以此实现用户信息的录入，应用于金融场景的用户身份认证，速度快，准确率高，减少用户输入成本，有效提高用户的体验</textarea> -->


  </div>
</template>

<script>
  export default {
    name: "IDCard",
    methods:{
      VerifyAcc(){
        if(this.GLOBAL.token===true){
          this.$router.push('/Controller/ControllerUseList')
        }else{
          this.$router.push('/login')
        }
      },
      VerifyAcc2(){
        if(this.GLOBAL.token===true){
          this.$router.push('/Controller/ControllerSDKDownload')
        }else{
          this.$router.push('/login')
        }
      }
    }
  }
</script>

<style scoped>
  body{
    font-size: 62.5%;
  }
  #apply{
    position: relative;
    left: 25%;
    bottom: 15%;
  }
  #download{
    position: relative;
    left: 47%;
    bottom: 15%;
  }
  .firstBackground{
    background-position: right bottom,left top;
    width: 100%;
    height: 50%;
    background-image: url("../assets/banner/身份证识别.jpg");
    background-size: 100% 100%;
  }
  .secondBackground{
    background-position: right bottom,left top;
    width: 100%;
    height: 50%;
    background-image: url("../assets/情感倾向分析/功能介绍.png");
    background-size: 100% 100%;
  }
  .functionButton{
    color: black;
    border-color: black;
    font-size:0.21rem;
    margin-top: 5.2rem;
  }

  .button4doc{
    margin-left:0.50rem;
    height: 0.50rem;
    width: 1.50rem;
    font-size: 0.22rem;
    color: white;border-width: 0.015rem;
    border-color: white;
    background-color: rgba(0,0,0,0);
    font-weight: 500;
    transition: all 0.3s;
  }

  .button4doc:hover{
    color: white;
    background-color: #262626;
  }


  .card4footer{
    background-image: url("../assets/短文本相似度/搜索引擎.png");
    width: 100%;
    height: 50%;
    background-size: 100% 100%;
    padding: 0;
  }

  .card4footer2{
    background-image: url("../assets/短文本相似度/生活服务.png");
    width: 100%;
    height: 50%;
    background-size: 100% 100%;
    padding: 0;
  }

  .title4card{
    margin-top: 0.14rem;
    font-size:0.21rem;
    text-align: center;
  }

  .content4card{
    width: 3rem;
    margin-left: auto;
    margin-right: auto;
    margin-top: 0.21rem;
    color: grey;
  }
  button{
    width: 2rem;
    height: 0.50rem;
    text-align: center;
    background: transparent;
    position: relative;
    bottom: 50%;
    right: 23%;
    border-color: white;
    color:white;
    font-size: 0.25rem;
    font-weight: lighter;
  }
  #titlecontent{
    background: transparent;
    color:white;
    position: relative;
    margin-left:2%;
    bottom: 65%;
    overflow:auto;
  }
  #introduce{
    font-size: 0.4rem;
    position: relative;
    margin-bottom:5%;
  }
  #introducecontent{
    position: relative;
    font-size:0.15rem;
    top: 12%;
  }
  #title{
    position: relative;
    bottom: 75%;
    left: 20%;
    font-size: 0.4rem;
    color: white;
    font-weight: lighter;
  }
  textarea{
    border: none;
    resize: none;
    background-color: white;
    color: black;
  }
  #carContent{
    position: relative;
    top: 0.05rem;
    left: 37.5%;
    width:24%;
    font-size:0.15rem;
    overflow:auto;
  }
  #carCaption{
    position: relative;
    top: 0.05rem;
    left: 28%;
    margin-bottom:0.1rem;
    margin-top:0.05rem;
    text-align: center;
    font-size:0.2rem;
    overflow: auto;
  }
  #serviceContent{
    position: relative;
    font-size:0.15rem;
    top: 0.05rem;
    left: 17.3%;
    width:24%;
    overflow:auto;
  }
  #serviceCaption{
    position: relative;
    top: 0.05rem;
    left: 14%;
    margin-bottom:0.1rem;
    margin-top:0.05rem;
    text-align: center;
    overflow: auto;
    font-size:0.2rem;
  }
  #txtApp{;
    font-size: 0.4rem;
    text-align: center;
  }
  body {
    margin: 0;
    padding: 0;
    height: 22rem;
  }
  .background {
    width:100%;
    height:100%;
    /*display: inline;*/
    /*position:absolute;*/
    /*z-index:0;*/
  }
  #AIcar{
    height: 2.50rem;
    width: 3rem;
    position: relative;
    padding-top: 0%;
    left: 18%;
    overflow: auto;
  }
  #AIcustomer{
    height: 2.5rem;
    width:3rem;
    position: relative;
    left: 40%;
    padding-top: 0%;
  }
  #AIhead{
    width: 100%;
    height: calc(25.8/100*23rem);

  }
  #AIbodyfir{
    width: 100%;
    height: calc(6.3/100*20rem);
    margin-top:0.5rem;
    padding: 0;
    background-size: auto 50%;
    text-align: center;
  }
  #AIbodysec{
    height: calc(22.8/100*23rem);
    margin: 0;
    padding: 0;
  }
  #AIbodythi{
    height: calc(27.6/100*23rem);
    margin-top:0.5rem;
    padding: 0;
  }
  #AItail{
    height: calc(10.5/100*23rem);
    margin: 0;
    padding: 0;
  }
</style>
