<template>
  <section class="py-7 reader-section">
    <div class="container px-3 px-lg-4 pt-xl-6">
      <h1>An ordinary story</h1>
      <p class="lead text-muted">Sometimes I write about web development, other times about random interesting stuff.</p>
      <div class="mt-5">
        <div class="blog">
          <BlogListItem v-bind:post="post" v-for="post of posts" :key="post.slug"/>
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
  head() {
    return {
      title: "Blogs"
    }
  }
};
</script>
