<template>
<div>
    <Banner />
    <HeaderDefault />
    <div class="body-content">
      <div class="body-course container">
        <Course />
        <Nuxt />
      </div>
    </div>
    <FooterDefault />
</div>
</template>

<script>
import HeaderDefault from '~/components/HeaderDefault'
import Banner from '~/components/Banner'
import Footer from '~/components/FooterDefault'
import Course from '~/components/course/CourseMenu';

export default {
methods: {
  },
  components: {
    HeaderDefault,
    Course,
    Banner,
    Footer,
  }
}
</script>

<style lang="scss">
.body-content {
  padding-bottom: 3rem;
  .body-course {
    width: 100%;
    display: flex;
    // .container {
    //   max-width: 1280px;
    // }
}
}

</style>