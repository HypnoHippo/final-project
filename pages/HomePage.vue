<template>
  <!-- Creating jumbotron and adding bootstrap classes for white text, padding, and font style -->
  <div id="jumbotron-container">
    <b-jumbotron text-variant="white" class="p-4" id="jumbotron">
      <div class="container p-5">
        <h1 class="display-4 font-weight-bold">Welcome to {{ title }}</h1>
        <p class="lead text-monospace">Your one stop for everything music!</p>
      </div>
    </b-jumbotron>

    <h4 class="mt-5">Here you can read up on music news, find free music, album art, and learn music facts!</h4>

    <!-- Adding continue button with bs classes for width, margin, and responsiveness -->
    <div class="container-fluid my-5">
      <b-button to="/MusicNews" class="w-50 my-5" id="continue-button">Continue</b-button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  data () {
    return {
      title: 'Music Splash'
    }
  },
  head () {
    return {
      title: this.title,
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: 'Music Splash',
          name: 'Music Splash',
          content: 'This is the landing page for Music Splash. Jump on in, the music is free!'
        }
      ]
    }
  }
}
</script>

<style>
  /* Changing colors of page items */
  #continue-button {
    background-color: #44b25d;
  }

  #jumbotron {
    background-image: url('@/static/jr-korpa.jpg');
    background-size: cover;
  }

  #jumbotron-container {
    background-color: #343a40;
  }
</style>
