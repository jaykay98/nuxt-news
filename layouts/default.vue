<template>
  <div>
    <NavBar />
    <div class="container mt-5 is-fullhd">
      <Nuxt />
    </div>
    <Footer />
  </div>
</template>

<script>
import NavBar from '../components/nav-bar.vue'
import Footer from '../components/footer.vue'
export default {
  name: 'DefaultLayout',
  components: { NavBar, Footer },
}
</script>

<style>
body {
  background-color: #3e32a8;
}
.container {
  display: flex;
  min-height: 100vh;
  flex-direction: column;
}
</style>