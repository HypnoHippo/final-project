<template>
  <div>
    <NavBar></NavBar>
      <div class="p-5">
        <h1 class="display-4">Lyrics Launch Pad</h1>
      </div>
    <AppFooter></AppFooter>
  </div>
</template>

<script>
import NavBar from '~/components/NavBar.vue'
import AppFooter from '~/components/AppFooter.vue'

export default {
  name: "LyricsPage",
  components: { NavBar, AppFooter }
}
</script>

<style>

</style>
