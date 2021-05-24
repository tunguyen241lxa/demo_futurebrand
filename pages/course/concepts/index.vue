<template>
<div>
  Hello concepts here
</div>

</template>

<script>
import CourseBetween from '~/components/course/contents/CourseBetween';

export default {
  head: {
    title: 'Concepts',
    meta: [
      {
        hid: 'concepts',
        name: 'concepts',
        content: 'Concepts description'
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