<template>



  <body>
  <div class="loginForm">
    <br>
    <h1 align="center">欢迎登录</h1>
    <form action="http://localhost:8080/maven_web_demo1_war_exploded/jsp/login.jsp" method="post">
      <table border="0" align="center">
        <tr><td>用户名：</td><td><input class="input" id="userName" name="userName" type="text" v-model="userName"></td></tr>
        <br>
        <tr><td>密&nbsp码：</td><td><input id="password" name="password" type="password"></td></tr>
        <br>
        <tr><td></td><td><router-link  to="/register"><el-button type="primary" > 注册</el-button></router-link> <el-button type="success" v-on:click="onLogin">登录</el-button></td></tr>
<!--        <input  type="text" v-model:value="userName"></input>-->
<!--        <el-button type="success" round icon="el-icon-check" v-on:click="onDeleteOrder"  circle></el-button>-->
      </table>
    </form>
  </div>
  </body>

</template>

<script>
  export default {
    name: "Login",
    data:function(){
      return{
        userName:""
      }
    },
    methods:{
      onLogin:function () {
        this.$message({
          message:'登录成功！',
          type:'success'
        });//query 相当于get 是明文传参
        this.$router.push({path:"/home",query:{"userName":this.userName}});
      },


    }
  }
</script>

<style scoped>
  body {
    width:100%;
    height:100%;
    position:fixed;
    background-image: url("../image/05.jpg");
    /* 背景图垂直、水平均居中 */
    background-position: center center;
    /* 背景图不平铺 */
    background-repeat: no-repeat;
    /* 当内容高度大于图片高度时，背景图像的位置相对于viewport固定 */
    background-attachment: fixed;
    /* 让背景图基于容器大小伸缩 */
    background-size: cover;
    /*添加动画*/
    animation-name: login-animation;
    /*动画执行时间*/
    animation-duration: 20s;
    /*动画延时时间*/
    animation-delay: 1.5s;
    /*动画开始时间 无限*/
    animation-iteration-count: infinite;
    /*动画循环播放*/
    animation-play-state: running;
  }

  /*添加动画*/
  @keyframes login-animation {
    0% {background: url("../image/01.jpg");
      /* 背景图垂直、水平均居中 */
      background-position: center center;
      /* 背景图不平铺 */
      background-repeat: no-repeat;
      /* 当内容高度大于图片高度时，背景图像的位置相对于viewport固定 */
      background-attachment: fixed;
      /* 让背景图基于容器大小伸缩 */
      background-size: cover;
    }
    25% {background: url("../image/02.jpg");
      /* 背景图垂直、水平均居中 */
      background-position: center center;
      /* 背景图不平铺 */
      background-repeat: no-repeat;
      /* 当内容高度大于图片高度时，背景图像的位置相对于viewport固定 */
      background-attachment: fixed;
      /* 让背景图基于容器大小伸缩 */
      background-size: cover;
    }
    50% {background: url("../image/01.jpg");
      /* 背景图垂直、水平均居中 */
      background-position: center center;
      /* 背景图不平铺 */
      background-repeat: no-repeat;
      /* 当内容高度大于图片高度时，背景图像的位置相对于viewport固定 */
      background-attachment: fixed;
      /* 让背景图基于容器大小伸缩 */
      background-size: cover;
    }
    75% {background: url("../image/02.jpg");
      /* 背景图垂直、水平均居中 */
      background-position: center center;
      /* 背景图不平铺 */
      background-repeat: no-repeat;
      /* 当内容高度大于图片高度时，背景图像的位置相对于viewport固定 */
      background-attachment: fixed;
      /* 让背景图基于容器大小伸缩 */
      background-size: cover;
    }
    100% {background: url("../image/01.jpg");
      /* 背景图垂直、水平均居中 */
      background-position: center center;
      /* 背景图不平铺 */
      background-repeat: no-repeat;
      /* 当内容高度大于图片高度时，背景图像的位置相对于viewport固定 */
      background-attachment: fixed;
      /* 让背景图基于容器大小伸缩 */
      background-size: cover;
    }
  }

  .loginForm {
    background: rgba(255,255,255,0.5);
    width: 400px;
    height:300px;
    margin: 200px auto;
  }
</style>
