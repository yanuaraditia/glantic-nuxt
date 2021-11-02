<template>
  <section class="py-5 reader-section">
    <div class="container px-4">
      <h2>{{ post.title }}</h2>
      <nuxt-content :document="post" />
    </div>
  </section>
</template>

<script>
export default {
  async asyncData({ $content, params, error }) {
    let post;
    try {
      post = await $content("blog", params.slug).fetch();
      // OR const article = await $content(`articles/${params.slug}`).fetch()
    } catch (e) {
      error({ message: "Blog Post not found" });
    }

    return {
      post,
    };
  },
  head() {
    return {
      title: this.post.title
    }
  }
};
</script>
