<template>
  <div id="app">
    <Nav />
    <!-- <div id="nav">
      <router-link to="/">Inicio</router-link> |
      <router-link to="/about">Información</router-link>
    </div> -->
    <router-view/>
  </div>
</template>

<script>
import Nav from '@/components/Nav.vue'
export default {
  components: {
    Nav
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  transition: all ease .4s;
}
@import 'scss/responsive';
#app {
  font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  // background: #000;
  padding: 0 3.5em;
  @media (max-width: $x-sm){
    padding: 0 1em;
  }

}

// #nav {
//   padding: 30px;

//   a {
//     font-weight: bold;
//     color: #2c3e50;

//     &.router-link-exact-active {
//       color: #42b983;
//     }
//   }
// }
</style>
