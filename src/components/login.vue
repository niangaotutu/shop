<template>
  <div class="login-wrap">
     
    <el-form class="login-form"   :label-position="labelPosition" label-width="80px" :model="formdata">
         <h2>用户登录</h2>
      <el-form-item label="用户名">
        <el-input v-model="formdata.name"></el-input>
      </el-form-item>
      <el-form-item label="密码">
        <el-input v-model="formdata.password"></el-input>
      </el-form-item>
       <el-button  class="login-btn" type="success">成功按钮</el-button>
    </el-form>
    
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
*{
    margin: 0;
    padding: 0
}
.login-wrap{
    background-color: pink;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center
}
.login-form{
    background-color: white;
    border-radius: 5px;
    width: 400px;
    padding: 30px
}
.login-btn{
    width: 100%;
}


</style>
