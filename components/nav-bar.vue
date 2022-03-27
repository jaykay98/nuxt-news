<template>
  <b-navbar centered fixed-top mobile-burger close-on-click shadow spaced>
    <template #brand>
      <b-navbar-item>
        <a href="/">NEWS WITH NUXT</a>
      </b-navbar-item>
    </template>
    <template #start>
      <b-navbar-item>
        <NuxtLink to="/">Home</NuxtLink>
      </b-navbar-item>
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