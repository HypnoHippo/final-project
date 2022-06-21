<template>
    <!-- Creating nav bar with Bs classes for item spacing and borders -->
    <b-nav justified class="nav">
        <!-- <NuxtLink>'s with child routes -->
        <NuxtLink to="/" exact exact-active-class="active" class="nav-item border-bottom border-right border-white">Home</NuxtLink>
        <NuxtLink to="/MusicNews" exact exact-active-class="active" class="nav-item border-left border-bottom border-white">News</NuxtLink>
        <NuxtLink to="/AlbumArt" exact exact-active-class="active" class="nav-item border-left border-bottom border-white">Album Art</NuxtLink>
        <NuxtLink to="/MusicFacts" exact exact-active-class="active" class="nav-item border-bottom border-left border-white">Music Facts</NuxtLink>
        <NuxtLink to="/VideosPage" exact exact-active-class="active" class="nav-item border-left border-bottom border-white">Free Music</NuxtLink>
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
    padding: 1rem;
  }

  li:hover, a:hover {
    background-image: linear-gradient( 109.6deg,  rgba(61,245,167,1) 11.2%, rgba(9,111,224,1) 91.1% );
    color: white;
    text-decoration: none;
  }
</style>
