<template>
  <b-navbar
    class="navbar"
    centered
    fixed-top
    mobile-burger
    close-on-click
    shadow
    spaced
  >
    <template #brand>
      <a href="/">NEWS WITH NUXT</a>
    </template>
    <template #start>
      <NuxtLink to="/">Home</NuxtLink>
      <b-navbar-item>
        <NuxtLink to="/about-us">About</NuxtLink>
      </b-navbar-item>
    </template>
  </b-navbar>
</template>

<style>
.nuxt-link-exact-active {
  border-bottom: 5px solid #07eb3c;
}
</style>