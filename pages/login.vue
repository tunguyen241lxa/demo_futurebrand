<template>
<div class="container">
  <a href="" class="title center"><mdicon name="home" class="mdi-ic"/>Trờ về trang chủ</a>
 <div class="table">
    <div class="content-center">
      <div class="form-login">
        

        <h3 class="brand">BRAND</h3>
        <label for="email">Email</label>
        <input type="email"/>

        <label for="password">Mật khẩu</label>
        <input type="password"/>

        <label for="checked"> 
          <input type="checkbox" checked="checked">
          Xác nhận lại mật khẩu
        </label>
      

        <button>Đăng nhập</button>
        <a class="forgot-password center">Quên mật khẩu</a>
        <div class="creat-account center">
          <label>Bạn chưa có tài khoản?</label>
          <a href="#">Tạo tài khoản</a>
        </div>
      </div>
    </div>
  </div>
</div>
 
</template>

<script>
export default {
  layout: "login"
}
</script>

<style lang="scss">
.container {
  .title {
    display: flex;
    justify-content: center;
    padding-bottom: 1rem!important;
    margin-bottom: 1.5rem!important;
    text-decoration: none;
  }
  .content-center {
    justify-content: center;
    display: flex;
    .form-login {
      flex-direction: column;
      display: flex;
      padding: 40px;
      border: solid 1px;
      border-radius: 20px;
      .brand::before {
      content: "FUTURE ";
      color: #e87821;
      }
      .brand {
        color: #35a606;
      }
      .brand::after {
        content: " VIỆT NAM";
        color: #1794c7;
      }
      .center {
        text-align: center;
      }
      input {
        outline: none
      }
      
      
      
     
    }
  }
}

</style>