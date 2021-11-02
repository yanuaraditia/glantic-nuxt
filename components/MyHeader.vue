<template>
  <nav class="navbar navbar-expand-lg navbar-light py-lg-3">
    <div class="container px-4">
      <nuxt-link class="navbar-brand" to="/">@yanuaraditia</nuxt-link>
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
            <nuxt-link class="nav-link" aria-current="page" to="/blogs">Blogs</nuxt-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>
