<template>
  <section class="py-7">
    <div class="container px-3 px-lg-4">
      <h1 class="h2">Blog posts</h1>
      <p>Sometimes I write about web development, other times about random interesting stuff.</p>
      <div class="mt-5">
        <div class="row">
          <div class="col-lg-4" v-for="post of posts" :key="post.slug">
            <div class="card bg-dark bg-opacity-25 link-top mb-4">
              <div class="card-body p-lg-4" style="min-height: 220px">
                <h3 class="card-title" v-html="post.title"></h3>
                <p class="card-text" v-html="post.description"></p>
              </div>
              <div class="card-footer p-lg-4">
                <span class="subheader fw-bold" v-html="toString(post.date)"></span>
              </div>
              <NuxtLink :to="`/blogs/`+post.slug"></NuxtLink>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const posts = await $content("blog")
      .sortBy('date','desc')
      .fetch();

    return {
      posts,
    };
  },
  methods: {
    toString(date) {
      const options = { year: 'numeric', month: 'long', day: 'numeric' }
      return new Date(date).toLocaleDateString('en', options)
    }
  },
  head() {
    return {
      title: "Blogs"
    }
  }
};
</script>
