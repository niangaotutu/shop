<template>

    <el-container class="container">
      <el-header>
          <el-row>
  <el-col :span="4">
      <img src="../assets/logo.png" alt="">
  </el-col>
  <el-col :span="19" class="middle"><h2>电商后台管理系统</h2></el-col>
  <el-col :span="1"><a href=""  class="exit">退出</a></el-col>
</el-row>
      </el-header>
      <el-container>
        <el-aside  class="aside" width="200px">Aside</el-aside>
        <el-main   class="main">Main</el-main>
      </el-container>
    </el-container>
 
</template>
<script>
export default {
    data(){

    return {
        
    }
    }
};
</script>
<style>
.container{
    background-color: #b3c0d1;
    height: 100%;
}
.aside{
    background-color: blue;
}
.main{
    background-color: red;
}
.middle{
    line-height: 60px;
    text-align: center;
    color:white;
}
.exit{
     line-height: 60px;
    text-align: center;
    text-decoration: none
}


</style>
