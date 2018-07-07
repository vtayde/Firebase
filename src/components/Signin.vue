<template>
  <div class="login-form" >
    <el-card class="login_card" >
      <p align="middle" class="Login_header">Sign in to Inside Insight</p>
      <form @submit.prevent="onSubmit" align="middle">
        <el-row class="input" :gutter="24">
          <el-col :span="3" :offset="3">
            <label align="left" class="label_feilds" for="email">Email</label>
          </el-col>
          <el-col :span="12" :offset="2">
            <input
              class="input_feilds"
              type="email"
              id="email"
              v-model="email">
          </el-col>
        </el-row>
        <br>
        <el-row class="input" :gutter="24">
          <el-col :span="3" :offset="3">
            <label class="label_feilds" for="password">Password</label>
          </el-col>
          <el-col :span="12" :offset="2">
            <input
              class="input_feilds"
              type="password"
              id="password"
              v-model="password">
            </el-col>
        </el-row>
        <br>
        <el-row :gutter="24">
          <el-col :span="6" :offset="8">
            <el-button class="submit_btn" @click="onSubmit()" :autofocus="false" >Submit</el-button>
          </el-col>
        </el-row>
      </form>
    </el-card>
  </div>
</template>
<script>
export default {
    data() {
        return {
            email: '',
            password: ''
        }
    },
    methods: {
        onSubmit () {
            console.log('Email', this.email)
            console.log('Password', this.password)
        }
    }
}
</script>
<style>
.Login_header {
  font-size: 2rem;
  color: white;

}
.login-form {
    position: relative;
    height: 100%;
    display: flex;
    justify-content: center;
    background: url('../assets/background_login7.jpg') no-repeat center center fixed;
    background-size: cover;
  }
 .ii-logo{
    width: 10em;
    margin: 5px auto;
    display: block;
  }
  .el-card.login_card {
    height: 322px;
    width: 40%;
    align-self: center;
    background-color: rgba(0, 0, 0, 0.4);
    border: 0px solid #030304;
  }

  .client-logo {
    display: block;
    margin: 0 auto;
  }
  #hint {
    font-size: 13px;
    color: rgba(0, 0, 0, 0.289);
  }
  .el-button--text{
    text-align: right;
  }
  .input {
    color: white;
    font-size: 18px;
  }
  .label_feilds {
    /* margin-right: 4rem */
    /* margin: 0.5rem; */
    margin: 1rem;
    padding-top: 10px;

  }
  .submit_btn {
    background-color: black;
    border: 1px solid white;
    color: white;
    width: 100%;
    height: 2.5rem;
    border-radius: 7px;
  }
  .input_feilds {
    border: 1px solid white;
    background-color: rgba(0, 0, 0, 0.5);
    height: 2rem;
    width: 100%;
    color: white;
    padding: 5px;
    border-radius: 7px;
  }
  .submit_btn:hover {
    background-color: black;
    border: 1px solid white;
    color: white;
  }
  .el-button.is-loading:before {
    pointer-events: none;
    content: '';
    position: absolute;
    left: -1px;
    top: -1px;
    right: -1px;
    bottom: -1px;
    border-radius: inherit;
    background-color: rgba(0, 0, 0, 0.35);
}
</style>
