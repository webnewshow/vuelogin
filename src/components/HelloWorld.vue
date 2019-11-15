<template>
  <div class="hello">
    <div class="login">
      <div class="title">LOGIN</div>
      <div class="user"><input type="text" name="user" placeholder="User"/></div>
      <div class="password"><input type="password" name="password" placeholder="Password"/></div>
      <div class="sign">Sign in</div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style >
body{
  background: #2980b9;
}
.login{
  width: 500px;
  height: 755px;
  margin: 0 auto;
  transform: perspective(800px) translate3d(0,20vh,0) rotate3d(2,0,0,70deg);
  border-left: 10px solid white;
  border-right: 10px solid white;
  background-color: #3d3d3d;
}
.login .title{
  font-weight: bold;
  font-size: 100px;
  text-align: center;
  color:#d35400;
  padding-top: 70px;
}
.login .user{
  text-align: center;
  margin-top: 80px;
}
.login .password{
  text-align: center;
  margin-top: 80px;
}
input[name="user"]{
  border: 3px solid  #d35400;
  outline-style: none;
  width: 350px;
  height: 70px;
  text-align: center;
}
input[name="password"]{
  border: 2px solid  #d35400;
  outline-style: none;
  width: 360px;
  height: 70px;
  text-align: center;
}
.sign{
  text-align: center;
  margin: 0 auto;
  margin-top: 80px;
  font-size: 100px;
  cursor: pointer;
  color:#d35400;
}
</style>
