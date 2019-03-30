<template>
  <div class="login-wrap">
    <el-form
      class="login-form"
      :label-position="labelPosition"
      label-width="80px"
      :model="formdata"
    >
      <h2>用户登录</h2>
      <el-form-item label="用户名">
        <el-input v-model="formdata.username"></el-input>
      </el-form-item>
      <el-form-item label="密码">
        <el-input v-model="formdata.password"></el-input>
      </el-form-item>
      <el-button @click.prevent="handleLogin" class="login-btn" type="success">登陆</el-button>
    </el-form>
  </div>
</template>
<script>
export default {
  data() {
    return {
      labelPosition: "top",
      formdata: {
        username: "",
        password: ""
      }
    };
  },
  methods: {
    // 发送登陆请求
    // handleLogin() {
    //   this.$http.post(`login`, this.formdata).then(res => {
    //     const {
    //       data: {
    //         data,
    //         meta: { status, msg }
    //       }
    //     } = res;
    //     if (status === 200) {
    //       // 渲染home组件
    //       // 改标示 js改标示 编程时导航
    //       this.$router.push({
    //         name: "home"
    //       });
    //     } else {
    //       this.$message.error(msg);
    //     }
    //   });
    // }
      async handleLogin() {
      var res = await this.$http.post(`login`, this.formdata)
       console.log(res)
      const {
          data: {
            data:{token,id,rid},
            meta: { status, msg }
          }
        } = res;
        if(status===200){
            // 把正确用户token保存
            localStorage.setItem('token',token)
            var a = localStorage.getItem("token")
            console.log(a)
            this.$router.push({
                name:"home"
            })
            
        }else{
            this.$message.error(msg);
        }
    }
  }
};
</script>
<style>
* {
  margin: 0;
  padding: 0;
}
.login-wrap {
  background-color: pink;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.login-form {
  background-color: white;
  border-radius: 5px;
  width: 400px;
  padding: 30px;
}
.login-btn {
  width: 100%;
}
</style>
