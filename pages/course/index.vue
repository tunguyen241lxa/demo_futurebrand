<template>
  <div class="course-body">
    <Course />
    <CourseContents />
    <div class="course-right"></div>
  </div>
</template>

<script>
import Course from '~/components/course/CourseMenu';
import CourseContents from '~/components/course/CourseContents';

export default {
  layouts: "default",

  components: {
    Course,
    CourseContents
  }
};
</script>

<style lang="scss">
.course-body {
    display: flex;
   
    
   
    .course-right {
        max-width: 16.666667%;
        height: 100%;
    }
}
</style>
