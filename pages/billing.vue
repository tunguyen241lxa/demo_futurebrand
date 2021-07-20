<template>
<div class="billing container">
  <h2>Bạn đăng ký khóa học</h2> 
  <div class="body">
    <div class="left">
      <h4><mdicon name="cart" class="mdi-ic"/>Giỏ hàng</h4>
      <div class="info">
        <!-- <h2>Nội dung</h2> -->
        <table>
          <thead>
            <tr>
              <th>#</th>
              <th>Nội dung</th>
              <th class="end">Thành tiền</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <th class="num pad-num">1</th>
              <td>
                <div class="book">
                  <span class="w-60"><img src="https://camp.brvn.vn/cover-300px/online/DTB_Cover_Thumb300_1618799099.jpg" alt="Não Trong Bão" class="shadow-2 rounded"></span>
                  <span></span>
                </div>
              </td>
              <td class="pri"><p>599,000</p></td>
            </tr>
            <tr class="bt-3">
              <td></td>
              <td class="cl">Tạm tính:</td>
              <td class="pri">599,000</td>
            </tr>
            <tr>
              <td></td>
              <td class="cl">Giảm giá:</td>
              <td class="pri">0d</td>
            </tr>
             <tr>
              <td></td>
              <td class="cl">Tổng cộng:</td>
              <td class="pri">599,000d</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
    <div class="right">
      <div class="bil-shadow">
        <div class="bil-content">
          <span>Tổng cộng(1 nội dung):</span>
          <h2>
            <span class="price">599,000</span>
            <sup>vnd</sup>
          </h2>
          <span class="text-fade">(đã bao gồm VAT)</span>
        </div>
        <footer>
          <button @click.prevent="openModal">Tiến hành thanh toán</button>
          
          <!-- <div id="myModal" class="modal"> -->

            <!-- Modal content -->
            <!-- <div class="modal-content"> -->
              <!-- <span class="close">&times;</span> -->
              <!-- <p>Some text in the Modal..</p> -->
            <!-- </div> -->

          <!-- </div> -->
        </footer>
      </div>

      <div class="bil-shadow margin">
        <div class="pad-top">
          <form>
            <input type="hidden">
            <div>
              <label>Mã ưu đãi / Mã giảm giá</label>
              <div class="input-group">
                <input type="text">
                <span><button>Áp dụng</button></span>
              </div>
            </div>
          </form>
        </div>
      </div>

    </div>
  </div>
  <div class="under-main-content">
    <div class="container">
      <h3>Khóa học mới nhất</h3>
    </div>
  </div>
  <!-- <v-modal name="test" /> -->
  <ModalCard />
</div>
</template>

<script>
import ModalCard from "~/components/billing/ModalCard"
export default {
  created () {
  },
  name: 'MyComponent',
    // mounted () {
        
    // },
  methods: {
    openModal() {
      //hooo
      console.log("Hi guys ....")
      this.$modal.show('example')
    }
    
    
  },
  components: {
    ModalCard
  }
}
</script>

<style lang="scss">
.margin {
  margin-top: 20px;
  .pad-top {
    padding-top: 10px!important;
    padding: 1.25rem;
    label {
      font-weight: 400;
      font-size: 12px;
      letter-spacing: .5px;
      display: inline-block;
      margin-bottom: .5rem;
    }
    .input-group {
      position: relative;
      display: -ms-flexbox;
      display: flex;
      -ms-flex-wrap: wrap;
      flex-wrap: wrap;
      -ms-flex-align: stretch;
      align-items: stretch;
      width: 100%;
      input {
        background-color: #fff;
        background-clip: padding-box;
        border: 1px solid #ced4da;
        position: relative;
        -ms-flex: 1 1 auto;
        flex: 1 1 auto;
        width: 1%;
        margin-bottom: 0;
        border-radius: 2px;
        color: #8b95a5;
        padding: 5px 12px;
        font-size: 14px;
        line-height: inherit;
        -webkit-transition: .2s linear;
        transition: .2s linear;
      }
      span {
        margin-left: -1px;
        display: flex;
        button {
          font-size: 12px;
          padding: 4px 12px;
          line-height: 20px;
          cursor: pointer;
          color: #71e271;
          border-color: #71e271;
          background-color: transparent;
          border-radius: 2px;
        }
      }
    }
  }
}
.billing {
  flex-direction: column;
  .body {
    display: flex;  
    .left {
      width: 70%;
      padding-right: 15px;
      padding-left: 15px;
      h4 {
        border-bottom: 1px solid #ebebeb !important;
        padding-bottom: 20px;
      }
      .info {
        table {
          width: 100%;
          max-width: 100%;
          margin-bottom: 1rem;
          background-color: transparent;
          thead {
            border-bottom: 3px solid #ebebeb!important;
            tr {
              th {
                padding: 10px 20px;
              }
              .end {
                display: flex;
                flex-direction: row-reverse;
              }
            }
          }
          tbody {
            .book {  
              .w-60 {
                width: 60px !important;
                img {
                  width: inherit;
                }
              }    
            }
            .bt-3 {
              border-top: 3px solid #ebebeb!important;
              
            }
            tr {
              border-top: 1px solid #ebebeb !important;
              .num {
                width: auto;
              }
              .pad-num {
                padding: 10px 20px;
              }
              .pri {
                padding: 10px 20px;
                display: flex;
                flex-direction: row-reverse;
              }
              th {
                padding: .75rem;
                vertical-align: top;
                // border-top: 1px solid #dee2e6;
              }
              td {
                padding: .75rem;
                vertical-align: top;
                // border-top: 1px solid #dee2e6;
                
              }
              .cl {
                width:70%;
                text-align: right;
              }
            }
          }
          
        }
      }
    }
    .right {
      width: 30%;
      .bil-shadow {
        -webkit-box-shadow: 0 0 25px rgb(0 0 0 / 7%);
        box-shadow: 0 0 25px rgb(0 0 0 / 7%);
        .bil-content {
          padding: 1.25rem;
          flex-direction: column;
          display: flex;
          text-align: center;
          h2 {
            .price {
              font-size: 35px!important;
              line-height: 1.2;
              color: #000!important;
          }
            sub {
              top: -1em;
              font-size: 18px!important;
              color: rgba(77,82,89,.7)!important;
            }
          }
        }
        footer {
          text-align: center;
          background-color: #fcfdfe;
          border-top: 1px solid rgba(77,82,89,.07);
          color: #8b95a5;
          padding: 10px 20px;
          button {
            background-color: #71e271;
            border: none;
            color: white;
            border-radius: 5px;
            padding: 10px 20px;
          }
        }
      }
    }
  }
}
</style>