<template>
<div class="container">
  <a href="/" class="title center"><mdicon name="home" class="mdi-ic"/>Trờ về trang chủ</a>
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
      

        <button class="btn-submit">Đăng nhập</button>
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
  methods: {
  },
  layout: "login"
}
</script>

<style lang="scss">
input:-webkit-autofill,
input:-webkit-autofill:hover, 
input:-webkit-autofill:focus,
textarea:-webkit-autofill:hover,
textarea:-webkit-autofill:focus,
select:-webkit-autofill,
select:-webkit-autofill:hover,
select:-webkit-autofill:focus {
  border: 1px solid #71e271;
  -webkit-text-fill-color: rgb(255, 255, 255);
  -webkit-box-shadow: 0 0 0px 1000px rgba(255, 255, 255, 0.1) inset;
  transition: background-color 5000s ease-in-out 0s;
}
.container {
  .title {
    display: flex;
    justify-content: center;
    padding-bottom: 1rem!important;
    margin-bottom: 1.5rem!important;
    text-decoration: none;
    color: #71e271;
  }
  .content-center {
    justify-content: center;
    display: flex;
    .form-login {
      flex-direction: column;
      box-shadow: -25px 0px 0px 0px #04daf0, -50px 0px 0 #f3b70f;
      display: flex;
      padding: 40px;
      // border: solid 1px;
      // background-color: #35a606;
      background: linear-gradient(to right, #33CB82, #71e271);
      // border-color: #35a606 !important;
      border-radius: 20px;
      label {
        color: white;
        margin-top: 1rem;
      }
      .brand::before {
      content: "FUTURE ";
      color: #ffffff;
      }
      .brand {
        color: #ffffff;
      }
      .brand::after {
        content: " VIỆT NAM";
        color: #ffffff;
      }
      .center {
        text-align: center;
      }
      .forgot-password {
        margin: 1rem;
        font-weight: bold;
      }
      input {
        outline: none;
        background-color: rgba(255, 255, 255, 0.1);
        // border: none;
        padding: 10px;
        font-size: 15px;
        border-radius: 10px;
        border: none;
        color: white;
      }
      .btn-submit {
        background: #f3b70f;
        border: none;
        // border-color: #fff !important;
        color: #fff !important;
        border-radius: 10px;
        font-size: 20px;
        padding: 10px;
        // font-weight: bold;
      }
      a {
        color: white;
      }
      .creat-account {
        label {
          color: white;
          
        }
        a {
          color: white;
        
        }
      }
      
      
     
    }
  }
}

</style>