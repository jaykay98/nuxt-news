<template>
  <div>
    <h1 class="title has-text-centered has-text-white">About Us</h1>
    <p class="subtitle has-text-centered has-text-white">
      The latest Australian news brought to you by
      <a
        href="https://newsapi.org/"
        target="_blank"
        class="
          news-api-link
          has-text-white has-text-weight-semibold
          is-underlined
        "
        >News API</a
      >
    </p>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'News with Nuxt - About Us',
    }
  },
}
</script>
