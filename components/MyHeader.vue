<template>
  <nav class="navbar navbar-expand-lg navbar-light py-lg-3" v-bind:class="showNav ? 'show' : 'hide'">
    <div class="container px-3 px-lg-4">
      <nuxt-link class="navbar-brand fw-medium" to="/">
        <span @click="resetNav">
        <svg xmlns="http://www.w3.org/2000/svg" class="text-primary" width="24" height="24" viewBox="0 0 24 24" fill="currentColor" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"></polygon></svg>
        yanuaraditia
        </span>
      </nuxt-link>
      <button class="navbar-toggler" type="button" @click="toggleNav()" v-bind:class="showNav ? 'active' : ''">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="navbar-collapse" v-bind:class="showNav ? 'show' : 'hide'">
        <ul class="navbar-nav ms-lg-auto mb-2 mb-lg-0">
          <li class="nav-item" @click="resetNav">
            <nuxt-link class="nav-link" aria-current="page" to="/">Home</nuxt-link>
          </li>
          <li class="nav-item" @click="resetNav">
            <nuxt-link class="nav-link" aria-current="page" to="/about">About Me</nuxt-link>
          </li>
          <li class="nav-item" @click="resetNav">
            <nuxt-link class="nav-link" aria-current="page" to="/blogs">Blog</nuxt-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>
<script>
export default {
  data() {
    return {
      showNav: false
    }
  },
  methods: {
    toggleNav() {
      this.showNav = !this.showNav
    },
    resetNav() {
      this.showNav = false
    }
  },
}
</script>
