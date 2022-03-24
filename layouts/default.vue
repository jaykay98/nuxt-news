<template>
  <div>
    <NavBar />
    <div class="container column is-10 is-fullhd">
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
