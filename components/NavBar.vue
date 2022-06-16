<template>
    <!-- Creating nav bar with Bs classes for item spacing and borders -->
    <b-nav justified class="nav">
        <!-- <b-nav-item>'s with child routes -->
        <b-nav-item to="/" exact exact-active-class="active" class="nav-item border-bottom border-right border-white">Home</b-nav-item>
        <b-nav-item to="/AlbumArt" exact exact-active-class="active" class="nav-item border-left border-bottom border-white">Album Art</b-nav-item>
        <b-nav-item to="/MusicFacts" exact exact-active-class="active" class="nav-item border-bottom border-left border-white">Music Facts</b-nav-item>
        <b-nav-item to="/VideosPage" exact exact-active-class="active" class="nav-item border-left border-bottom border-white">Free Music</b-nav-item>
    </b-nav>
</template>

<script>
export default {
  name: 'NavBar'
}
</script>

<style scoped>
  /* styling nav items and adding hover effect */
  a {
    color: white;
    background-color: #343a40;
  }

  li:hover, a:hover {
    background-image: linear-gradient( 109.6deg,  rgba(61,245,167,1) 11.2%, rgba(9,111,224,1) 91.1% );
    color: white;
  }
</style>
