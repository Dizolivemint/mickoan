<template>
  <div class="about">
    <Header></Header>
    <div class="ml-4">
      <h1>About</h1>
    </div>
    <div class="card">
      <div class="card-body">
        <div class="card-text">
          Koans are Zen poems often containing some paradoxical logic or hidden wisdom. Contemplating a koan is said to lead to enlightenment. As the mind attempts to solve the koan, one can experience profound levels of creativity. Koans often have Asian characters and settings, taking place hundreds of years ago. This website is dedicated to modern koans that contain imagery of our modern society.
        </div>
      </div>
    </div>
    <hr>
    <Footer></Footer>
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/root/Header.vue'
import Footer from '@/components/root/Footer.vue'

export default {
  name: 'home',
  components: {
    Header,
    Footer
  }
}
</script>