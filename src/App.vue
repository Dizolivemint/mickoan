<template>
  <div id="app">
    <router-view :posts="posts"/>
  </div>
</template>

<script>
export default {
  data: () => ({
    posts: [
      { 
        id: 0,
        content: 'An astronaut watches an asteroid and comments "paint job needs to be fixed". A voice echos "fixed". A woman watches.',
        category: 'space' 
      },
      { 
        id: 1,
        content: 'An astronaut watches an asteroid and comments "paint job needs to be fixed". A voice echos "fixed". A woman watches.',
        category: 'space' 
      }
    ]
  })
}
</script>


<style lang="scss">
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
