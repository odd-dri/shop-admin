<template>

  <el-row type="flex" class="row-bg" justify="center" align="middle">
  <el-col :xs="14" :sm="12" :md="10" :lg="8" :xl="6">
    <el-form ref="loginForm" class="login-form" :model="form" label-position="top" label-width="80px">
        <el-form-item label="用户名">
          <el-input v-model="form.username" label-position="top"></el-input>
        </el-form-item>
        <el-form-item label="密码">
          <el-input v-model="form.password"></el-input>
        </el-form-item>
        
        
        <el-form-item>
          <el-button type="primary" size="medium" @click="onSubmit">登录</el-button>
          <el-button size="medium">重置</el-button>
        </el-form-item>
      </el-form>
  </el-col>
</el-row>

  
</template>

<script>
  export default {
    data() {
      return {
        form: {
          username: 'admin',
          password: '123456'
        }
      }
    },
    methods: {
      onSubmit() {
        console.log('submit!');
      }
    }
  }
</script>
 <style>
  .row-bg {
    height: 100%;
    background-color: #2D434C;
  }

  .login-form {
    border-radius: 8px;
    background-color: #fff;
    padding: 30px 20px;
    min-width: 400px;
  }
 </style>
 