<template>
  <div class="course-between">
      <h2 id="s1">Khóa học đầu tiên</h2>

      <!-- <b-img-lazy v-bind="mainProps" :src="getImageUrl(80)" alt="Image 1"></b-img-lazy> -->
      <p>To get started quickly you can use the create-nuxt-app.

          Make sure you have npx installed (npx is shipped by default since npm 5.2.0) or npm v6.1 or yarn.
      </p>
       <!-- <video-embed css="embed-responsive-21by9" src="https://www.youtube.com/watch?v=s4ObxcdXoFE"></video-embed> -->

      <!-- <iframe width="420" height="345" src="https://www.youtube.com/embed/tgbNymZ7vqY"></iframe> -->

      <youtube-media :video-id="videoId" style="padding-top: 2rem"></youtube-media>

      <h2 id="s2">Bonus step</h2>
      <p>
        Create a page named fun.vue in the pages directory.

        Add a template and include a heading with a funny sentence inside.

        Then, go to your browser and see your new page on localhost:3000/fun.
      </p>
      
      <h2 id="s3">Create your first page</h2>
      <p>Nuxt.js transforms every *.vue file inside the pages directory as a route for the application.</p>
      <h6 class="author">Tác Giả</h6>
      <h8 class="author">Nguyễn Thị Cẩm Tú</h8>
    </div>
</template>


<script>


export default {

  // props: [ "video-id" ],
  data() {
      return {
        // mainProps: {
        //   center: true,
        //   fluidGrow: true,
        //   blank: true,
        //   blankColor: '#bbb',
        //   width: 600,
        //   height: 400,
        //   class: 'my-5'
        // },
      videoId: '2au7dg-MYPg',

      }
    },
    props: ['object', 'property'],
    mounted() {
      
    },
    methods: {
      // getImageUrl(imageId) {
      //   const { width, height } = this.mainProps
      //   return `https://picsum.photos/${width}/${height}/?image=${imageId}`
      //   // return `~/assets/img/demoyoutb.PNG`
      // },
      
      method(url) {
        
        this.videoId = this.$youtube.getTimeFromURL(url)
        this.startTime = this.$youtube.getTimeFromURL(url)
      }
    },
    
   
}
</script>

<style lang="scss">
.course-between {
  width: 75%;
  h2 {
    padding-top: 2rem;
  }
  p {
    padding-bottom: 0px;
    margin-bottom: 0px;
    text-align: justify;
    text-justify: inter-word;
  }
  h6 {
    padding-top: 2rem;
  }
}
.author {
  display: flex;
  justify-content: flex-end;
}
</style>