<template>
  <div class="course-body">
    <!-- <Course /> -->
    <!-- <CourseContents /> -->
    <CourseBetween />
    <div class="icon" id="social-contact">
      <ul class="social-right">
        <li><a href="" ><mdicon name="facebook" class="mdi-ic"/></a></li>
        <li><a href="" ><mdicon name="twitter" class="mdi-ic"/></a></li>
        <li><a href="" ><mdicon name="instagram" class="mdi-ic"/></a></li>
     
      </ul>
    </div>
    <div class="course-right">
      <h5>Nội dung</h5>
      <a
        href="#"
        class="first after"
        :class="{ active: isActive == 'course' }"
        @click="openMenu('course')"
        v-scroll-to="{ el: '#s1', offset: -90 }"
        style="border-bottom: 1px dashed #e6e6e6;"
        >Khóa học đầu tiên</a
      >
      <a
        href="#"
        class="first after"
        :class="{ active: isActive == 'step' }"
        @click="openMenu('step')"
        v-scroll-to="{ el: '#s2', offset: -80 }"
        style="border-bottom: 1px dashed #e6e6e6;"
        >Bonus step</a
      >
      <a
        href="#"
        class="first after"
        :class="{ active: isActive == 'step3' }"
        @click="openMenu('step3')"
        v-scroll-to="{ el: '#s3', offset: -80 }"
        style="border-bottom: 1px dashed #e6e6e6;"
        >Create your first page</a
      >
      <!-- <button type="button" class="btn btn-success">Success</button> -->
      
    </div>
  </div>
</template>

<script>
import CourseBetween from "~/components/course/contents/CourseBetween";
// import { mdiFacebook } from '@mdi/js';

// import { mdiAlphaABox } from '@mdi/js';
export default {
  layout: "course",
  layout(context) {
    return "course";
  },
   asyncData() {
    console.info("Hello")
  },
  // validate(context) {
  //   //eslint-disable-next-line no-console
  //   console.log(context)

  //   return /^[0-9]{9-12}$/.test(context.params.hid)
  // },
  data() {
    return {
      isOpen: true,
      isActive: "home"
    };
  },
  head: {
    title: "Course",
    meta: [
      {
        hid: "course",
        name: "course",
        content: "Course description"
      }
    ]
  },
  
  mounted() {
    this.$nextTick(function() {
      window.addEventListener("scroll", function() {
        var navbar = document.getElementById("social-contact");
        var nav_classes = navbar.classList;
        if (
          document.documentElement.scrollTop >= 100 &&
          document.documentElement.scrollTop <= 600
        ) {
          if (nav_classes.contains("media") === false) {
            nav_classes.toggle("media");
          }
        } else {
          if (nav_classes.contains("media") === true) {
            nav_classes.toggle("media");
          }
        }
      });
    });
  },
  
  methods: {
    openClose() {
      this.isOpen = !this.isOpen;
    },
    async openMenu(item) {
      // this.isOpen = !this.isOpen;
      this.isActive = item;
    }
  },
  components: {
    CourseBetween
  }
};
</script>

<style lang="scss">
.course-body {
  display: flex;

  width: 100%;

  .course-between {
    // max-width: 50%;
    height: 100%;
    padding: 15px;
    padding-top: 2rem;
    padding-left: 1rem;
    padding-right: 1rem;
    h2 {
      color: #2f495e;
      font-weight: 500;
      position: relative;
      // font-size: 2.25rem;
      display: table;
      font-family: sans-serif;
      margin-bottom: 1.5rem;
    }
  }
  .icon {
      width: 5%;
      ul {
        padding-top: 150px;
      
      
   
      top: 0px;
     
      // height: 100%;
      padding-bottom: 20px;

        list-style: none;
        padding-left: 0px;
         a {
        color: #1c1c1f;
        cursor: pointer;
        }
        a:hover {
          color: #71e271;
        }
      }
      
     
    }
  .media {
    ul {
      position: -webkit-sticky;
      position: sticky;
    }
    
  
  }
  .course-right {
    flex-direction: column;
    width: 20%;
    padding-top: 2rem;

    display: flex;

    a {
      -webkit-backface-visibility: hidden;
      backface-visibility: hidden;
      position: relative;
      transition: 0.5s color ease;
      text-decoration: none;
      color: #1f2529;
      font-size: 15px;
      padding-top: .5rem;
      padding-bottom: .5rem;
      &:hover {
        color: #71e271;
      }

      &.active {
        color: #71e271;
      }
    }

    img {
      width: 25px;
    }
    
  }
}
</style>
