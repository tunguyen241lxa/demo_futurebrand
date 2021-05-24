<template>
<div>
  Hello feature here
</div>

</template>

<script>
import CourseBetween from '~/components/course/contents/CourseBetween';

export default {
   head: {
    title: 'Feature',
    meta: [
      {
        hid: 'feature',
        name: 'feature',
        content: 'Feature description'
      }
    ],
  },
  props: {
  },
  layout: "course",
  layout (context) {
    return 'course'
  },

  components: {
    CourseBetween
  }
};
</script>