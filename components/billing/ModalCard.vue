<template>
  <foo name="example" :width="500" :height="450">
    <div class="modal-body">
      <div class="info-user">
        <span class="avatar">
          T
        </span>
        <div class="media-body">
          <span >
            <button class="close" @click.prevent="closeModal">x</button>
          </span>
          <h5>
            Nguyễn Thị Cẩm Tú
          </h5>
        </div>
      </div>
      <p class="mb-10 mt-10">Thanh toán trực tiếp bằng:</p>
      <form>
        <a class="btn-success">Thẻ tín dụng qua cổng AsiaPay</a>
      </form>
      <p class="mb-10 mt-10">Bạn có thể thanh toán bằng thẻ tín dụng VISA hoặc MasterCard</p>
      <p >
        <img class="w-100px" src="https://www.brandcamp.asia/build/img/credit-card.png" alt="visa" />
      </p>
      <a class="btn-success">Thẻ nội địa qua cổng OnePay</a>
      <p class="mb-10 mt-10">Bạn phải có thông tin thẻ và tài khoản Internet Banking</p>
      <p>
        <img class="w-full" src="https://www.brandcamp.asia/build/img/OPATM.PNG" alt="card" />
      </p>
      <form>
        <a class="btn-success">Ví điện tử Momo</a>
      </form>
    </div>
  </foo>
</template>

<script>
export default {
  methods: {
    closeModal() {
      this.$modal.hide('example');
    }
  }
}
</script>

<style lang="scss">
.modal-body {
  position: relative;
  -ms-flex: 1 1 auto;
  flex: 1 1 auto;
  padding: 1rem;
  .info-user {
    border-bottom: 3px solid #ebebeb!important;
    padding: 16px 12px;
    -webkit-transition: background-color .2s linear;
    transition: background-color .2s linear;
    padding-left: 0!important;
    padding-right: 0!important;
    padding-top: 0!important;
    display: flex;
    -ms-flex-align: start;
    align-items: flex-start;
    .avatar {
      flex-shrink: 0;
      background-color: #71e271!important;
      color: #fff;
      margin: 0 8px;
      position: relative;
      display: inline-block;
      width: 36px;
      height: 36px;
      line-height: 36px;
      text-align: center;
      border-radius: 100%;
      background-color: #f5f6f7;
      // color: #a3a3a3;
      text-transform: uppercase;
    }
    .media-body {
      span {
        .close {
          padding: 0;
          background-color: transparent;
          border: 0;
          -webkit-appearance: none;
          font-weight: 400;
          outline: none!important;
          -webkit-transition: .2s linear;
          float: right;
          font-size: 1.2rem;
          line-height: 1;
          color: #000;
          text-shadow: 0 1px 0 #fff;
          opacity: .5;
        }
      }
      h5 {
        font-size: 16px;
        font-weight: 400;
        letter-spacing: -.1px;
      }
    }
  }
  .mb-10 {
    margin-bottom: 10px!important;
  }
  .mt-10 {
    margin-top: 10px!important;
  }
  p {
    .w-100px {
      width: 100px!important;
      max-width: 100%;
      vertical-align: middle;
      border-style: none;
    }
  }
  p {
    .w-full {
      width: 100%!important;
      max-width: 100%;
      vertical-align: middle;
      border-style: none;
    }
  }
  // form {
    .btn-success {
      cursor: pointer;
      background-color: #71e271;
      border-color: #71e271;
      display: block;
      width: 100%;
      font-size: 14px;
      padding: 5px 16px;
      letter-spacing: 1px;
      border-radius: 2px;
      line-height: inherit;
      outline: none!important;
      transition: .15s linear;
      font-weight: 400;
      text-align: center;
      white-space: nowrap;
      vertical-align: middle;
      user-select: none;
      border: 1px solid transparent;
    }
  // }
}
</style>