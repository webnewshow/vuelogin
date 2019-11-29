<template>
  <div class="hello">
    <div class="box">
      <div class="register clearfix">
        <form>
        <div class="title">REGISTER</div>
        <div class="user">
          <input type="text" name="user" placeholder="User" />
        </div>
        <div class='code clearfix'>
          <input type="text" name='code' placeholder="Code"/><span class="getCode">获取验证码</span>
        </div>    
        <div class="password">
          <input type="password" name="password" placeholder="Password" />
        </div>
        <div class="passwordAgain">
          <input type="password" name="passwordAgain" placeholder="PasswordAgain" />
        </div>
        <div class="signUp">Sign up</div>
        <div class="goLo">login</div>
        </form>
      </div>
      <div class="login clearfix">
        <form>
        <div class="title">LOGIN</div>
        <div class="user" >
          <input type="text" name="user" placeholder="User" />
        </div>
        <div class="password">
          <input type="password" name="password" placeholder="Password" />
        </div>
        <div class="signIn">Sign in</div>
        <div class="goRe magin-30">register</div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
   mounted() {
     let goRe=document.querySelector('.goRe');
     let goLo=document.querySelector('.goLo');
     let box = document.querySelector('.box')
     goRe.onclick=function(){
        box.classList.add('on');
     };
     goLo.onclick=function(){
        box.classList.remove('on');
     }
   }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style >
body {
  background: #2980b9;
}
*{
  box-sizing: border-box;
}
.clearfix::after{
  content:"";
  display: block;
  clear: both; 
  visibility: hidden;
}
.hello {
  transform: perspective(800px) translate3d(0,20vh,0) rotate3d(2,0,0,70deg);
  height: 720px;
  overflow: hidden;
  width: 540px;
  margin: 0 auto;
}
.box {
  position: relative;
  top: -720px;
  transition: 1s;
}
.box.on{
  top: 0px;
  transition: 1s;
}
.goRe,.goLo{
  color: white;
  float:right;
  padding: 0 10px;
  cursor: pointer;
}
.login,
.register {
  width: 530px;
  height: 720px;
  margin: 0 auto;
  border-left: 10px solid white;
  border-right: 10px solid white;
  background-color: #3d3d3d;
}
.login .title,
.register .title {
  font-weight: bold;
  font-size: 100px;
  text-align: center;
  color: #d35400;
  padding-top: 50px;
}
.register .title{
  padding-top: 30px;
}
.login .user,.login .password {
  text-align: center;
  margin-top: 80px;
}
.register .user,.register .password,.register .code,.register .passwordAgain{
  text-align: center;
  margin-top: 20px;
}
.register .code{
  padding: 0px 60px;
}
input[name="user"]{
  border: 3px solid #d35400;
  outline-style: none;
  width: 350px;
  height: 70px;
  text-align: center;
}
input[name="password"],input[name='passwordAgain'] {
  border: 3px solid #d35400;
  outline-style: none;
  width: 360px;
  height: 70px;
  text-align: center;
}
.register input[name="password"]{
  width: 370px;
}
input[name='passwordAgain']{
  width: 380px;
}
input[name='code']{
  border: 3px solid #d35400;
  outline-style: none;
  width: 200px;
  height: 70px;
  text-align: center;
}
.getCode{
  cursor: pointer;
  color: #d35400;
  font-size: 30px;
  margin-left: 10px;
  float:right;
  line-height: 70px;
}
.signIn,.signUp{
  text-align: center;
  margin: 0 auto;
  margin-top: 70px;
  font-size: 100px;
  cursor: pointer;
  color: #d35400;
}
.signUp{
  margin-top: 20px;
}
</style>
