<template>
  <div>
    <NavBar />
    <div class="p-5">
      <h1 class="display-4 mb-5">
        Music News
      </h1>
      <b-card-group v-if="stories" deck class="d-flex flex-row justify-content-around">
        <NewsArticle
          v-for="story in computedObj"
          :key="story.id"
          :story="story"
        />
      </b-card-group>
    </div>
    <AppFooter />
  </div>
</template>

<script>
import axios from 'axios'
import NavBar from '~/components/NavBar.vue'
import AppFooter from '~/components/AppFooter.vue'
import NewsArticle from '~/components/NewsArticle.vue'

export default {
  name: "MusicNews",
  components: { NavBar, AppFooter, NewsArticle },
  data () {
    return {
      loading: true,
      stories: null,
      errored: false,
      limit: 9
    }
  },
  computed: {
    computedObj () {
      return this.limit ? this.stories.slice(0, this.limit) : this.stories
    }
  },
  mounted () {
    axios
      .get('https://newsapi.org/v2/everything?q=music&pageSize=10&apiKey=638de38889a74faf9148c19761885b51')
      .then(response => (this.stories = response.data.articles))
      .catch(error => {
        console.log(error)
        this.errored = true
      })
      .finally(() => { this.loading = false })
  }
}
</script>

<style>
  /* #articles-container {
    display: flex;
  }

  .card-deck {
    justify-content: center;
  } */
</style>
