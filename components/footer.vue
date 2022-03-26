<template>
  <footer class="footer">
    <div class="content has-text-centered">
      <p>
        Data provided by
        <a href="https://newsapi.org/" target="_blank">News API</a>
      </p>
      {{ new Date().getFullYear() }} —
      <strong>Jason Kidd</strong>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'FooterItem',
}
</script>

<style>
</style>