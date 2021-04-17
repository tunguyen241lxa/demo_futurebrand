<template>
  <div class="container contain">
    <div class="home-row">
      <div class="home-left">
        <Logo />
      </div>
      <!-- <h1 class="title">
        Future Brand Vietnam
      </h1> -->
      <div class="links home-right">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          rel="noopener noreferrer"
          class="button--green"
        >
          Why Future Brand Việt Nam ?
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          rel="noopener noreferrer"
          class="button--grey"
        >
          GET STARTED
        </a>
        
      </div>
    </div>
  </div>
</template>

<script>
export default {
  
}
</script>

<style lang="scss">

.container {
  margin: 0 auto;
  min-height: 100vh;
  // display: flex;
  // justify-content: center;
  // align-items: center;
  // text-align: center;
  
  .home-row {
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;

    .home-left {
      // display: ;
      width: 40%
    }

    .home-right {
      width: 60%;
      .subtitle {
        font-weight: 300;
        font-size: 42px;
        color: #526488;
        word-spacing: 5px;
        padding-bottom: 15px;
      }

      .links {
        padding-top: 15px;
      }
    }
  }
  
  // .title {
  //   font-family:
  //     'Quicksand',
  //     'Source Sans Pro',
  //     -apple-system,
  //     BlinkMacSystemFont,
  //     'Segoe UI',
  //     Roboto,
  //     'Helvetica Neue',
  //     Arial,
  //     sans-serif;
  //   display: block;
  //   font-weight: 300;
  //   font-size: 100px;
  //   color: #35495e;
  //   letter-spacing: 1px;
  // }

  
}

.contain {
  padding: 40px 40px 30px;
}

</style>
