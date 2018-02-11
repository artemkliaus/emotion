<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style lang="stylus">
* {
  margin: 0;
  padding: 0;
  border: 0;
  outline: 0;
}

body {
  background-image url(./assets/header_background.png)
  background-repeat no-repeat
  background-position right top
  padding-left 20px
  padding-right 20px
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
