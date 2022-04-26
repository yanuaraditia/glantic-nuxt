<template>
  <nav class="navbar navbar-expand-lg py-lg-3" v-bind:class="[(showNav ? 'show' : 'hide'),($nuxt.$colorMode.preference === 'dark' ? 'navbar-dark' : 'navbar-light')]">
    <div class="container px-3 px-lg-4">
      <button class="navbar-toggler border-0 no-shadow" type="button" @click="toggleNav()" v-bind:class="[($nuxt.$colorMode.preference === 'dark' ? 'text-light' : 'text-dark'),(showNav ? 'active' : '')]">
        <svg xmlns="http://www.w3.org/2000/svg" class="icon" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><line x1="4" y1="8" x2="20" y2="8" /><line x1="4" y1="16" x2="20" y2="16" /></svg>
      </button>
      <nuxt-link class="navbar-brand fw-medium" to="/">
        <span @click="resetNav" class="text-primary">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="currentColor" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"></polygon></svg>
        </span>
        <span @click="resetNav">yanuaraditia</span>
      </nuxt-link>
      <button type="button" style="box-shadow: none" class="navbar-toggler border-0 no-shadow" @click="$nuxt.$colorMode.preference = ($nuxt.$colorMode.preference === 'dark' ? 'light' : 'dark')" v-bind:class="[($nuxt.$colorMode.preference === 'dark' ? 'text-light' : 'text-dark')]">
        <svg xmlns="http://www.w3.org/2000/svg" v-if="$nuxt.$colorMode.preference === 'light'" class="icon" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><circle cx="12" cy="12" r="4" /><path d="M3 12h1m8 -9v1m8 8h1m-9 8v1m-6.4 -15.4l.7 .7m12.1 -.7l-.7 .7m0 11.4l.7 .7m-12.1 -.7l-.7 .7" /></svg>
        <svg xmlns="http://www.w3.org/2000/svg" v-else class="icon" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M12 3c.132 0 .263 0 .393 0a7.5 7.5 0 0 0 7.92 12.446a9 9 0 1 1 -8.313 -12.454z" /></svg>
      </button>
      <div class="navbar-collapse" v-bind:class="showNav ? 'show' : 'hide'">
        <ul class="navbar-nav ms-lg-auto mb-2 mb-lg-0">
          <li class="nav-item" @click="resetNav">
            <nuxt-link class="nav-link fw-medium" aria-current="page" to="/">Home</nuxt-link>
          </li>
          <li class="nav-item" @click="resetNav">
            <nuxt-link class="nav-link fw-medium" aria-current="page" to="/about">About Me</nuxt-link>
          </li>
          <li class="nav-item" @click="resetNav">
            <nuxt-link class="nav-link fw-medium" aria-current="page" to="/blogs">Blog</nuxt-link>
          </li>
          <li class="nav-item" @click="resetNav">
            <nuxt-link class="nav-link fw-medium" aria-current="page" to="/projects">Project</nuxt-link>
          </li>
          <li class="nav-item" @click="resetNav">
            <nuxt-link class="nav-link fw-medium" aria-current="page" to="/contact">Contact</nuxt-link>
          </li>
          <li class="nav-item d-none d-lg-inline" @click="resetNav">
            <button type="button" style="box-shadow: none" class="nav-link btn px-lg-3 no-shadow" @click="$nuxt.$colorMode.preference = ($nuxt.$colorMode.preference === 'dark' ? 'light' : 'dark')">
              <svg xmlns="http://www.w3.org/2000/svg" v-if="$nuxt.$colorMode.preference === 'light'" class="icon" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><circle cx="12" cy="12" r="4" /><path d="M3 12h1m8 -9v1m8 8h1m-9 8v1m-6.4 -15.4l.7 .7m12.1 -.7l-.7 .7m0 11.4l.7 .7m-12.1 -.7l-.7 .7" /></svg>
              <svg xmlns="http://www.w3.org/2000/svg" v-else class="icon" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M12 3c.132 0 .263 0 .393 0a7.5 7.5 0 0 0 7.92 12.446a9 9 0 1 1 -8.313 -12.454z" /></svg>
            </button>
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
