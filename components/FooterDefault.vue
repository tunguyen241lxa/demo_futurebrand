<template>
    <div class="footer">
      <!-- <b-card bg-variant="success" text-variant="white" header="Success" class="text-center footer">
        <b-card-text>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</b-card-text>
      </b-card> -->
      <div class="mx-auto px-4 px-4 container">
        <section class="mail-section">
          <h2>Tin Tức <span>Brand</span></h2>
          <p>Nhận tin tức Future Brand Việt Nam mới nhất vào hộp thư đến của bạn, được quản lý bởi nhóm Future Brand Việt Nam.</p>
          <form class="form-email">
            <div class="inline">
              <label class="label-email">Email</label>
              <input placeholder="Email" type="email" id="news-email" aria-label="Newsletter" required="required" class="email"/>
            </div>
            <input type="submit" name="subscribe" value="Subscribe" class="subscribe"/>
          </form>
        </section>
      </div>
      <div class="bg-footer">
        <div class="container">
          <div class="logo">
            <img src="~/static/img/brand.png" alt="Kitten">
          </div>
          <div class="info-feature">
            <div class="introduction info-3 info-left">
                <b-navbar-nav>
                  <h3>Hello world</h3>
                    <b-nav-item href="/course" >Getting started</b-nav-item>
                    <b-nav-item href="" >Components</b-nav-item>
                    <b-nav-item href="" >Icons</b-nav-item>
                </b-navbar-nav>
            </div>
            <div class="introduction info-3 info-between">
              
                <b-navbar-nav>
                                <h3>Hello world</h3>

                    <b-nav-item href="/course" >Getting started</b-nav-item>
                    <b-nav-item href="" >Components</b-nav-item>
                    <b-nav-item href="" >Icons</b-nav-item>
                </b-navbar-nav>
            </div>
            <div class="introduction info-3 info-right" style="text-align:end"> 
                <b-navbar-nav>
                                <h3>Hello world</h3>

                    <b-nav-item href="/course" >Getting started</b-nav-item>
                    <b-nav-item href="" >Components</b-nav-item>
                    <b-nav-item href="" >Icons</b-nav-item>
                </b-navbar-nav>
            </div>
          </div>
        </div>
      </div>
      
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss">
.footer {
  bottom: 0;
  display: block;
  background-color: #f8f9fa;
  box-shadow: inset 0px 5px 5px -5px#9f9898;
  // background-color: #f8f9fa ;
  .bg-footer {
    background-color: #1c1c1f;
    padding-top: 3rem;
    padding-bottom: 3rem;
    box-shadow: 0 -5px 5px -5px #9f9898;
    .container {
      max-width: 1280px;
      .logo {
        display: flex;
        justify-content: center;
      }
      .info-feature {
        display: flex;
        margin-top: 2rem;
        .introduction {
          .navbar-nav {
            color: white;
            .nav-item {
              .nav-link {
                color: white;;
              }
              .nav-link:hover {
                // --text-opacity: 1;
                color: #35a606;
                // color: rgba(0,197,142,var(--text-opacity));
              }
            }
          }
        }
        .info-3 {
          width: 33.333333%;
        }
        .info-left {
          text-align: left;
        }
        .info-between {
          text-align: center;
        }
        .info-right {
          text-align: end;
        }
      }
    }
  }
  
  
  
  
}


  .px-4 {
    padding-left: 1rem;
    padding-right: 1rem;
    .mail-section {
      text-align: center;
      padding-top: 5rem;
      padding-bottom: 5rem;
      padding-left: .75rem;
      padding-right: .75rem;
      .form-email {
        display: flex;
        justify-content: center;
        .inline {
          display: inline-block;
          .label-email {
            display: none;
          }
          .email {
            width: 16rem;
            padding-left: 1rem;
            padding-right: 1rem;
            padding-top: .75rem;
            padding-bottom: .75rem;
            outline: 2px solid transparent;
            outline-offset: 2px;
            border-width: 1px 0px 1px 1px;
            border-radius: 0.25rem 0rem 0rem 0.25rem;
            line-height: inherit;
            font-size: 100%;
            overflow: visible;
            box-sizing: border-box;
            border-style: solid;
            border-color: #d6dfec;
          }
          
        }
      }
      
      .subscribe {
          // left: 800px;
          // position: absolute;
          text-transform: uppercase;
          box-shadow: 0 1px 3px 0 rgb(0 0 0 / 10%), 0 1px 2px 0 rgb(0 0 0 / 6%);
          padding-left: 1rem;
          padding-right: 1rem;
          padding-top: .5rem;
          font-size: 1rem;
          font-weight: 500;
          display: inline-block;
          padding-bottom: .5rem;
          cursor: pointer;
          border-top-left-radius: 0;
          border-bottom-left-radius: 0;
          border-width: 0;
          background-color: #71e271;
          border-radius: .25rem;
          line-height: inherit;
          font-family: inherit;
          --text-opacity: 1;
          color: #fff;
          color: rgba(255,255,255,var(--text-opacity));
          padding-top: 0.75rem;
          padding-bottom: 0.75rem;
          box-shadow: 0 1px 3px 0 rgb(0 0 0 / 10%), 0 1px 2px 0 rgb(0 0 0 / 6%);
        }
      h2 {
        span::before {
          content: "Future ";
          color: #e87821;
        }
        span::after {
          content: " Việt Nam";
          color: #1794c7;
        }
        span {
          color:#35a606;
        }
      }
    }
  }
  
  .mx-auto {
      margin-left: auto;
      margin-right: auto;
  }

</style>