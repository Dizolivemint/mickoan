<template>
  <div class="home">
    <div v-for="(x, index) in 2" :key="index" :class="`bg-strips strip-${index}`"></div>
    <div class="bg-color-overlay"></div>

    <Header></Header>
     <!-- Main Content -->
     <div class="container">
      <div class="row p-3">
        <div v-for="(post, index) in posts" :key="index" class="col-md-6 mx-auto">
          <div class="m-5 card">
            <p  class="mt-4 p-3 post">
              {{ post.content }}
            </p>
          </div>
        </div>
      </div>
    </div>
    <Footer></Footer>
  
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/root/Header.vue'
import Footer from '@/components/root/Footer.vue'

export default {
  name: 'home',
  props: ['posts'],
  components: {
    Header,
    Footer
  },
  data: () => ({})
}
</script>

<style lang="scss">

  .home, .bg-strips, .bg-color-overlay, Footer {
    margin: auto;
    max-width: 1680px;
    .card {
      background-color: #0c1144d7;
      // min-width: 40%;
      -webkit-box-shadow: -3px 5px 30px -9px rgba(0,0,0,1);
      -moz-box-shadow: -3px 5px 30px -9px rgba(0,0,0,1);
      box-shadow: -3px 5px 30px -9px rgba(0,0,0,1);

    }
  }

  .bg-color-overlay {
    min-height: 1360px;
  }

  .bg-strips {
    width: 100vw;
    height: 100vh;
    position: absolute;
    min-height: 1360px;
  }
  .strip-0 {
    background-color: rgb(97, 0, 0);
    -webkit-clip-path: polygon(50% 5%, 61% 35%, 95% 35%, 68% 57%, 80% 95%, 50% 70%, 20% 95%, 32% 57%, 5% 35%, 39% 35%);
    clip-path: polygon(50% 5%, 61% 35%, 95% 35%, 68% 57%, 80% 95%, 50% 70%, 20% 95%, 32% 57%, 5% 35%, 39% 35%);
  }
  .strip-1 {
    background-color: rgb(16, 12, 56);
    -webkit-clip-path: polygon(0% 0%, 0% 100%, 5% 100%, 5% 5%, 95% 5%, 95% 95%, 5% 95%, 5% 100%, 100% 100%, 100% 0%);
    clip-path: polygon(0% 0%, 0% 100%, 5% 100%, 5% 5%, 95% 5%, 95% 95%, 5% 95%, 5% 100%, 100% 100%, 100% 0%);
  }
  .bg-color-overlay {
    opacity: .1;
    background-color: #97a4df;
    background-attachment: fixed;
    width: 100%;
    height: 100%;
    position: fixed;
  }
  Footer {
    position: fixed;
    bottom: 0;
    width: 100%;
  }
</style>
