<template>
  <section class="py-5 reader-section">
    <div class="container px-3 px-lg-4 pt-xl-6">
      <h1 class="h2">{{ post.title }}</h1>
      <div class="my-3 text-muted">
        <span v-html="toString(post.date)"></span>
        <span>•</span>
        <span>{{reading_time}} minute read</span>
      </div>
      <div id="article">
        <nuxt-content :document="post" />
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
  data() {
    return {
      reading_time: 1
    }
  },
  head() {
    return {
      title: this.post.title
    }
  },
  mounted() {
    const text = document.getElementById("article").innerText
    const wpm = 225
    const words = text.trim().split(/\s+/).length
    const time = Math.ceil(words / wpm);
    this.reading_time = time
  },
  methods: {
    toString(date) {
      const options = { year: 'numeric', month: 'long', day: 'numeric' }
      return new Date(date).toLocaleDateString('en', options)
    }
  },
};
</script>
