<template>
  <section class="section">
    <div v-for="(article, index) in newsArticles.articles" :key="index">
      <h3>{{ article.title }}</h3>
    </div>
  </section>
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
      `https://newsapi.org/v2/top-headlines?country=au&apiKey=f982225deff14ca1b46cbb4a1dbba64f`
    ).then((res) => res.json())
  },
  head() {
    return {
      title: 'News with Nuxt - Home',
    }
  },
}
</script>
