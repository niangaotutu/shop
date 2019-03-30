<template>
  <div class="login-wrap">
      <h2>用户登录</h2>
    <el-form class="login-form"   :label-position="labelPosition" label-width="80px" :model="formdata">
      <el-form-item label="用户名">
        <el-input v-model="formdata.name"></el-input>
      </el-form-item>
      <el-form-item label="密码">
        <el-input v-model="formdata.password"></el-input>
      </el-form-item>
     
    </el-form>
     <el-button  class="login-btn" type="success">成功按钮</el-button>
  </div>
</template>
<script>
export default {
    data(){
        return {
          labelPosition: 'top',
          formdata: {
          name: '',
          password: '',
        }
    }
}};
</script>
<style>
</style>
