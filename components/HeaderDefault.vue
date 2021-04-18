<template>
  <div>
  <b-navbar class ="nav-brand-future" toggleable="lg" type="light" variant="light">
    <b-navbar-brand class="brand noHover headder-left" href="#">BAND</b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" class="header-right" is-nav>
      <b-navbar-nav class="header-center">
        <b-nav-item href="#">
          TRANG CHỦ
        </b-nav-item>
        <b-nav-item href="#" >VỀ CHÚNG TÔI</b-nav-item>
        <b-nav-item href="#" >KHÓA HỌC</b-nav-item>
        <!-- <b-nav-item href="#" disabled>BLOG</b-nav-item> -->
        <b-nav-item-dropdown text="BLOG" right>
          <b-dropdown-item href="#">BRANDING</b-dropdown-item>
          <b-dropdown-item href="#">MARKETING</b-dropdown-item>
        </b-nav-item-dropdown>
        <b-nav-item href="#" >EBOOK</b-nav-item>
        <!-- <b-nav-item href="#" >TUYỂN DỤNG</b-nav-item> -->

      </b-navbar-nav>

      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto header-right-mini">
        <b-nav-form>
          <toggle-button class="toggle" v-model="myDataVariable"/>

          <!-- <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input> -->
          <!-- <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button> -->
        </b-nav-form>

        <!-- <b-nav-item-dropdown text="Lang" right>
          <b-dropdown-item href="#">EN</b-dropdown-item>
          <b-dropdown-item href="#">VI</b-dropdown-item>
        </b-nav-item-dropdown> -->

        <b-nav-item-dropdown right>
          <!-- Using 'button-content' slot -->
          <template #button-content>
            <em>User</em>
          </template>
          <b-dropdown-item href="#">Lang</b-dropdown-item>
          <b-dropdown-item href="#">Profile</b-dropdown-item>
          <b-dropdown-item href="#">Sign Out</b-dropdown-item>
        </b-nav-item-dropdown>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</div>
</template>

<script>
export default {
  data() {
    return {
      myDataVariable: null,
    }
  },
}
</script>

<style lang="scss">


.nav-brand-future {
  // overflow: hidden;
  height: 40px;
  padding: 10px 60px;
  background-color: rgb(255, 255, 255);
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
    color:#35a606;
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

</style>