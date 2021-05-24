<template>
  <div id="nav">
    <div class="container">
      <!-- <b-navbar class ="nav-brand-future dynamic-subtitles z-30" toggleable="lg" type="light" variant="light"> -->
      <b-navbar
        class="nav-brand-future dynamic-subtitles z-30"
        toggleable="lg"
        type="light"
      >
        <!-- <div> -->
        <b-navbar-brand class="brand noHover headder-left" href="#"
          >BRAND</b-navbar-brand
        >

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" class="header-right" is-nav>
          <b-navbar-nav class="header-center" >
            <b-nav-item class="header" >
              <NuxtLink
                class="header-item"
                :class="{'active': isOpen == 'home'}"
                @click.native="openClose('home')"
                to="/"
                >TRANG CHỦ</NuxtLink
              >
            </b-nav-item>
            <b-nav-item class="header"
              ><NuxtLink
                class="header-item"
                :class="{'active': isOpen == 'about'}"
                @click.native="openClose('about')"
                to="/about-us"
                >VỀ CHÚNG TÔI</NuxtLink
              ></b-nav-item
            >
            <b-nav-item class="header">
              <NuxtLink
                class="header-item"
                :class="{'active': isOpen == 'course'}"
                @click.native="openClose('course')"
                to="/course"
                >KHÓA HỌC
              </NuxtLink>
            </b-nav-item>
            <!-- <b-nav-item href="#" disabled>BLOG</b-nav-item> -->
            <b-nav-item-dropdown
              class="header"
              @click="openClose('blog')"
              text="BLOG"
              right
            >
              <b-dropdown-item href="#">BRANDING</b-dropdown-item>
              <b-dropdown-item href="#">MARKETING</b-dropdown-item>
            </b-nav-item-dropdown>
            <b-nav-item
              class="header"
              @click="openClose"
              href="#"
              >EBOOK</b-nav-item
            >
            <!-- <b-nav-item href="#" >TUYỂN DỤNG</b-nav-item> -->
          </b-navbar-nav>

          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto header-right-mini">
            <b-nav-form>
              <toggle-button id="toggle" class="toggle" v-model="darkMode" />
            </b-nav-form>

            <b-nav-item-dropdown right>
              <!-- Using 'button-content' slot -->
              <template #button-content>
                <em>User</em>
              </template>
              <b-dropdown-item href="#">Lang</b-dropdown-item>
              <b-dropdown-item href="#">Billing</b-dropdown-item>
              <b-dropdown-item href="#">Profile</b-dropdown-item>
              <b-dropdown-item href="#"><NuxtLink  to="/login">Login</NuxtLink></b-dropdown-item>

            </b-nav-item-dropdown>
          </b-navbar-nav>
        </b-collapse>
        <!-- <div/> -->
      </b-navbar>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      darkMode: false,
      isOpen: 'home',

      isActive: false
    }
  },
  mounted() {
    // set 'app-background' class to body
    let bodyElement = document.body;
    bodyElement.classList.add("app-background");

    let htmlElement = document.documentElement;
    let theme = localStorage.getItem("theme");

    if (theme === "dark") {
      htmlElement.setAttribute("theme", "dark");
      this.darkMode = true;
    } else {
      htmlElement.setAttribute("theme", "light");
      this.darkMode = false;
    }

    // add class shink in attribute id = nav
    this.$nextTick(function() {
      window.addEventListener("scroll", function() {
        var navbar = document.getElementById("nav");
        var nav_classes = navbar.classList;
        if (document.documentElement.scrollTop >= 100) {
          if (nav_classes.contains("shadow") === false) {
            nav_classes.toggle("shadow");
          }
        } else {
          if (nav_classes.contains("shadow") === true) {
            nav_classes.toggle("shadow");
          }
        }
      });
    });
  },
  watch: {
    darkMode: function() {
      // add/remove class to/from html tag
      let htmlElement = document.documentElement;

      if (this.darkMode) {
        localStorage.setItem("theme", "dark");
        htmlElement.setAttribute("theme", "dark");
      } else {
        localStorage.setItem("theme", "light");
        htmlElement.setAttribute("theme", "light");
      }
    }
  },
  methods: {
    async openClose(menuItem) {
      // this.isOpen = !this.isOpen;
      this.isOpen = menuItem
      
    },
    // isActive: function (menuItem) {
    //   return this.isOpen === menuItem
    // },
  }
};
</script>

<style lang="scss">
@import "@/assets/css/styles.scss";
.shadow {
  // box-shadow: 0 1px 3px 0 rgb(0 0 0 / 10%), 0 1px 2px 0 rgb(0 0 0 / 6%);
  position: fixed;
  top: 0;
  z-index: 999;
  background: white;
  width: 100%;
}
.container {
  // background-color: #f8f9fa !important;
  max-width: 1280px;
  .z-30 {
    top: 0;
    z-index: 30;
  }
  .nav-brand-future {
    // overflow: hidden;
    height: 40px;
    padding: 10px 60px;
    // background-color: rgb(255, 255, 255);
    position: fixed;
    position: relative;
    top: 0;
    width: 100%;
    a.brand::before {
      content: "FUTURE ";
      color: #e87821;
    }
    a.brand::after {
      content: " VIỆT NAM";
      color: #1794c7;
    }
    a.brand {
      color: #35a606;
    }
    a.noHover {
      pointer-events: none;
    }
    .header-left {
      width: 20%;
    }
    .header-right {
      width: 80%;

      .header-center {
        margin: auto;
        .header {
          .header-item {
            color: rgba(0, 0, 0, 0.5);
            text-decoration: none;
          }
          .nuxt-link-exact-active {
            color: #35a606 !important;
          }
        }
        
      }
      .header-right-mini {
        width: 20%;
        justify-content: center;
      }
    }
    .toggle {
      margin-right: 0.5rem !important;
    }
  }
}
</style>
