<template>
  <!-- Creating jumbotron and adding bootstrap classes for white text, padding, and font style -->
  <div id="jumbotron-container">
    <b-jumbotron text-variant="white" class="p-4" id="jumbotron">
      <div class="container p-5">
        <h1 class="display-4">Welcome to Music Mania</h1>
        <p class="lead">Your one stop for everything music!</p>
      </div>
    </b-jumbotron>

    <h4 class="mt-5">Here you can read up on music news, find free music, album art, and learn music facts!</h4>

    <!-- Adding continue button with bs classes for width, margin, and responsiveness -->
    <div class="container-fluid my-5">
      <b-button to="/AlbumArt" class="w-50 my-5" id="continue-button">Continue</b-button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomePage'
}
</script>

<style>
  /* Changing colors of page items */
  #continue-button {
    background-color: #44b25d;
  }

  #jumbotron {
    background-image: url('@/static/sandro-katalina.jpg');
    background-size: cover;
  }

  #jumbotron-container {
    background-color: #343a40;
  }
</style>
