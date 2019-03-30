<template>
  <el-container class="container">
    <el-header>
      <el-row>
        <el-col :span="4">
          <img src="../assets/logo.png" alt>
        </el-col>
        <el-col :span="19" class="middle">
          <h2>电商后台管理系统</h2>
        </el-col>
        <el-col :span="1">
          <a href class="exit">退出</a>
        </el-col>
      </el-row>
    </el-header>
    <el-container>
      <el-aside class="aside" width="200px">
        <el-menu  class="el-menu-vertical-demo" :unique-opened="true" :router='true'>
          <el-submenu index="1">
            <template slot="title">
              <i class="el-icon-location"></i>
              <span>用户管理</span>
            </template>
            <el-menu-item index="1-1">
              <i class="el-icon-info"></i>
              <span>用户列表</span>
            </el-menu-item>
          </el-submenu>

          <el-submenu index="2">
            <template slot="title">
              <i class="el-icon-location"></i>
              <span>权限管理</span>
            </template>
            <el-menu-item index="1-1">
              <i class="el-icon-sort-down"></i>
              <span>角色列表</span>
            </el-menu-item>
              <el-menu-item index="1-1">
              <i class="el-icon-star-on"></i>
              <span>权限列表</span>
            </el-menu-item>
          </el-submenu>

          <el-submenu index="3">
            <template slot="title">
              <i class="el-icon-location"></i>
              <span>商品管理</span>
            </template>
            <el-menu-item index="1-1">
              <i class="el-icon-service"></i>
              <span>商品列表</span>
            </el-menu-item>
             <el-menu-item index="1-1">
              <i class="el-icon-service"></i>
               <span>分类参数</span>
            </el-menu-item>
             <el-menu-item index="1-1">
              <i class="el-icon-service"></i>
               <span>商品分类</span>
            </el-menu-item>
          </el-submenu>

          <el-submenu index="4">
            <template slot="title">
              <i class="el-icon-location"></i>
              <span>订单管理</span>
            </template>
             <el-menu-item index="1-1">
              <i class="el-icon-info"></i>
              <span>订单列表</span>
            </el-menu-item>
          </el-submenu>

           <el-submenu index="5">
            <template slot="title">
              <i class="el-icon-location"></i>
              <span>数据统计</span>
            </template>
             <el-menu-item index="1-1">
              <i class="el-icon-info"></i>
              <span>数据报表</span>
            </el-menu-item>
          </el-submenu>
        </el-menu>
      </el-aside>
      <el-main class="main">Main</el-main>
    </el-container>
  </el-container>
</template>
<script>
export default {
  data() {
    return {};
  }
};
</script>
<style>
.container {
  background-color: #b3c0d1;
  height: 100%;
}
/* .aside{
} */
.main {
  background-color: red;
}
.middle {
  line-height: 60px;
  text-align: center;
  color: white;
}
.exit {
  line-height: 60px;
  text-align: center;
  text-decoration: none;
}
</style>
