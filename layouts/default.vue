<template>
  <div>
    <NavBar />
    <div class="container column is-10 is-fullhd">
      <Nuxt />
    </div>
  </div>
</template>

<script>
import NavBar from '../components/nav-bar.vue'
export default {
  name: 'DefaultLayout',
  components: { NavBar },
  data() {
    return {
      items: [
        {
          title: 'Home',
          icon: 'home',
          to: { name: 'index' },
        },
        {
          title: 'Inspire',
          icon: 'lightbulb',
          to: { name: 'inspire' },
        },
      ],
    }
  },
}
</script>
