<template>
  <div>
    <p v-if="$fetchState.pending" class="has-text-centered">
      Grabbing news articles...
    </p>
    <p v-else-if="$fetchState.error" class="is-danger has-text-centered">
      Oops! Looks like something went wrong
    </p>
    <div
      v-for="(article, index) in newsArticles.articles"
      v-else
      :key="index"
      class="card mb-6"
    >
      <header class="card-header">
        <p class="card-header-title is-centered title">{{ article.title }}</p>
      </header>
      <div class="card-image is-centered">
        <img
          :src="article.urlToImage"
          width="100%"
          alt="An image of the news article content"
        />
      </div>
      <div class="card-content">
        <div class="content">
          {{ article.description }}
        </div>
        <div class="content">
          <time>{{ article.publishedAt.toLocaleString() }}</time>

          <footer class="card-footer">
            <a :href="article.url" target="_blank" class="card-footer-item"
              >Open in New Tab</a
            >
          </footer>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      newsArticles: [],
    }
  },
  async fetch() {
    this.newsArticles = await fetch(
      `https://newsapi.org/v2/top-headlines?country=au&apiKey=${process.env.NUXT_ENV_NEWS_API_KEY}`
    ).then((res) => res.json())
  },
  head() {
    return {
      title: 'News with Nuxt - Home',
    }
  },
}
</script>
