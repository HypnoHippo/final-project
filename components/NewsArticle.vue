<template>
  <div id="card-container">
    <b-card
      :img-src="story.urlToImage"
      img-alt="Article Image"
      img-top
      tag="article"
      style="max-width: 30rem;"
      class="mb-5"
      img-width="480px"
    >
      <template #header>
        <h4>
          {{ story . title }}
        </h4>
      </template>
      <b-card-text class="text-dark mt-3">
        {{ story.description }}
      </b-card-text>
      <template #footer>
        <b-button block :href="story.url" variant="primary">
          Go to Article
        </b-button>
      </template>
    </b-card>
  </div>
</template>

<script>
export default {
  name: "NewsArticle",
  props: {
    story: {
      type: Object,
      required: true
    }
  }
}
</script>

<style>
  #card-container {
    display: flex;
    flex: 1 1 auto;
    justify-content: center;
  }
</style>
