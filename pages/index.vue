<template>
  <!-- Adding in router view and components -->
  <div id="app">
    <nav-bar></nav-bar>
    <HomePage></HomePage>
    <app-footer></app-footer>
  </div>
</template>

<script>
import HomePage from './HomePage.vue'
import NavBar from '@/components/NavBar.vue'
import AppFooter from '@/components/AppFooter.vue'

export default {
  name: 'IndexPage',
  title: 'Index',
  components: {
    NavBar,
    AppFooter,
    HomePage
  },
  head () {
    return {
      title: this.title,
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: 'Index Page',
          name: 'Index Page',
          content: 'This is the landing page for Music Splash. Jump on in, the music is free!'
        }
      ]
    }
  }
}
</script>

<style lang="scss">

// Giving page not covered by components a dark background
body {
  background-color: #343a40;
}

// Adding dark bg, aligning text, and making text white on all pages
#app {
 text-align: center;
 background-color: #343a40;
 color: white;
}

// Styling nav bar and items
nav {
  padding: 30px;
  a {
    font-weight: bold;
  }
}

.nav-link {
  width: 100%;
  padding: 1rem;
}

// Making display class text responsive
@media screen and (max-width: 1200px) {
  .display-4 {
    font-size: calc(1.475rem + 2.7vw);
  }
}
</style>
