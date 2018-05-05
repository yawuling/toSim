<template>
  <div class="page">
    <div class="draggable">
      <div class="header-menu">
        <i class="iconfont icon-menu"></i>
        <i class="iconfont icon-minimize"></i>
        <i class="iconfont icon-close"></i>
      </div>
      <img class="logo" src="../assets/img/logo.png" />
    </div>
    <div class="content">
      <el-input
        class="login-input"
        size="medium"
        placeholder="账号"
        v-model="username">
      </el-input>
      <el-input
        class="login-input"
        type="password"
        size="medium"
        placeholder="密码"
        v-model="password">
      </el-input>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Login',
  data() {
    return {
      username: '',
      password: ''
    }
  }
}
</script>

<style lang="scss" scoped>
.page {
  width: 350px;
  height: 400px;
  background: #fff;
  overflow: hidden;

  .header-menu {
    padding: 12px;
    text-align: right;
  }
  .logo {
    display: block;
    width: 84px;
    height: 84px;
    margin: 8px auto;
  }
  .iconfont {
    margin-left: 14px;
  }
  .content {
    width: 256px;
    margin: 0 auto;
  }
  .login-input {
    margin-bottom: 16px;    

    &:last-child {
      margin-bottom: 18px;
    }
    & /deep/ input {
      border-color: #bfcbd9;

      &::-webkit-input-placeholder{
        color:#8492a6;
      }
    }
  }
}
.draggable {
  width: 100%;
  height: 158px;
  -webkit-app-region: drag;
}

</style>
