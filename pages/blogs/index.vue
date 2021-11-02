<template>
  <section class="py-7">
    <div class="container px-4">
      <h1>All Posts</h1>
      <div class="mt-3">
        <div class="link-top" v-for="post of posts" :key="post.slug">
          <div class="row">
            <div class="col-lg-2 pt-lg-2">
              <span class="subheader fw-bold text-muted" v-html="toString(post.createdAt)"></span>
            </div>
            <div class="col-lg">
              <h3 class="card-title" v-html="post.title"></h3>
              <p class="card-text" v-html="post.description"></p>
            </div>
          </div>
          <NuxtLink :to="`/blogs/`+post.slug"></NuxtLink>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const posts = await $content("blog").fetch();

    return {
      posts,
    };
  },
  methods: {
    toString(date) {
      const options = { year: 'numeric', month: 'long', day: 'numeric' }
      return new Date(date).toLocaleDateString('id', options)
    }
  },
  head() {
    return {
      title: "Blogs"
    }
  }
};
</script>
