<template>
  <div class="blog-item">
    <div class="card blog-card border- bg-opacity-50 link-top mb-4" v-bind:class="[($nuxt.$colorMode.preference === 'dark' ? 'bg-dark' : 'bg-light')]">
      <div class="card-body p-lg-4">
        <h3 class="card-title h5" v-html="post.title"></h3>
        <p class="card-text" v-html="post.description"></p>
      </div>
      <div class="card-footer border-0 bg-transparent px-4 pb-4">
        <div>
          <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-calendar-minus" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
            <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
            <rect x="4" y="5" width="16" height="16" rx="2"></rect>
            <line x1="16" y1="3" x2="16" y2="7"></line>
            <line x1="8" y1="3" x2="8" y2="7"></line>
            <line x1="4" y1="11" x2="20" y2="11"></line>
            <line x1="10" y1="16" x2="14" y2="16"></line>
          </svg>
          <span class="subheader fw-bold" v-html="toString(post.date)"></span>
        </div>
      </div>
      <NuxtLink :to="`/blogs/`+post.slug"></NuxtLink>
    </div>
  </div>
</template>

<script>
export default {
  name: "BlogListItem",
  props: [
    'post'
  ],
  methods: {
    toString(date) {
      const options = { year: 'numeric', month: 'long', day: 'numeric' }
      return new Date(date).toLocaleDateString('en', options)
    }
  },
}
</script>
