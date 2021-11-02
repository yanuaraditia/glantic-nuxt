<template>
  <section class="py-5 reader-section">
    <div class="container px-3 px-lg-4">
      <div class="mx-lg-auto" style="max-width: 768px">
        <h1>{{ post.title }}</h1>
        <div class="mt-5">
          <nuxt-content :document="post" />
        </div>
      </div>
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
