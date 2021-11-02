<template>
  <nav class="navbar navbar-expand-lg navbar-light py-lg-3">
    <div class="container px-4">
      <nuxt-link class="navbar-brand fw-medium" to="/">
        <svg xmlns="http://www.w3.org/2000/svg" class="text-primary" width="24" height="24" viewBox="0 0 24 24" fill="currentColor" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"></polygon></svg>
        yanuaraditia
      </nuxt-link>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <nuxt-link class="nav-link" aria-current="page" to="/">Home</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link class="nav-link" aria-current="page" to="/about">About Me</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link class="nav-link" aria-current="page" to="/blogs">Blog</nuxt-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>
