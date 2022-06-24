<template>
  <div>
    <NavBar />
    <div class="p-5">
      <h1 class="display-4 mb-5">
        {{ title }}
      </h1>
      <h5 class="text-white text-center mb-5">Click an article to mark it as read!</h5>
      <b-card-group v-if="stories" deck class="d-flex flex-row justify-content-around">
        <NewsArticle
          v-for="story in stories"
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
      title: 'Music News'
    }
  },
  mounted () {
    axios
      .get('https://newsapi.org/v2/everything?q=music&pageSize=9&apiKey=638de38889a74faf9148c19761885b51')
      .then(response => (this.stories = response.data.articles))
      .catch(error => {
        console.log(error)
        this.errored = true
      })
      .finally(() => { this.loading = false })
  },
  head () {
    return {
      title: this.title,
      meta: [
        {
          hid: 'Music News',
          name: 'Music News',
          content: "This page features the top news articles about music from around the web, all compiled right here!"
        }
      ]
    }
  }
}
</script>

<style>
@media screen and (max-width: 575px) {
  .card-deck {
    display: block;
  }
}
</style>
