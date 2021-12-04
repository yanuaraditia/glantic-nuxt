<template>
  <nav class="navbar navbar-expand-lg navbar-dark py-lg-3" v-bind:class="showNav ? 'show' : 'hide'">
    <div class="container px-3 px-lg-4">
      <button class="navbar-toggler border-0 text-white no-shadow" type="button" @click="toggleNav()" v-bind:class="showNav ? 'active' : ''">
        <svg xmlns="http://www.w3.org/2000/svg" class="icon" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><line x1="4" y1="8" x2="20" y2="8" /><line x1="4" y1="16" x2="20" y2="16" /></svg>
      </button>
      <nuxt-link class="navbar-brand fw-medium" to="/">
        <span @click="resetNav">
        <svg xmlns="http://www.w3.org/2000/svg" class="text-primary" width="24" height="24" viewBox="0 0 24 24" fill="currentColor" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"></polygon></svg>
        yanuaraditia
        </span>
      </nuxt-link>
      <nuxt-link to="/" class="d-lg-none">
        <svg xmlns="http://www.w3.org/2000/svg" class="icon text-white" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M19 8.71l-5.333 -4.148a2.666 2.666 0 0 0 -3.274 0l-5.334 4.148a2.665 2.665 0 0 0 -1.029 2.105v7.2a2 2 0 0 0 2 2h12a2 2 0 0 0 2 -2v-7.2c0 -.823 -.38 -1.6 -1.03 -2.105" /><path d="M16 15c-2.21 1.333 -5.792 1.333 -8 0" /></svg>
      </nuxt-link>
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
          <li class="nav-item" @click="resetNav">
            <nuxt-link class="nav-link" aria-current="page" to="/projects">Project</nuxt-link>
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
