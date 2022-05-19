<template>
  <section class="py-5 reader-section">
    <div class="container px-3 px-lg-4 pt-xl-6">
      <div class="top-img bg-primary overflow-hidden bg-opacity-10 main-radius">
        <img :src="post.img" alt="" style="transform: translateX(2rem) translateY(2rem)">
      </div>
      <div class="mt-5">
        <h1 class="h3" v-text="`Project: ${post.title}`"></h1>
        <p class="lead text-muted" v-text="post.description"></p>
        <div class="div">
          <div v-for="tag in post.tags" :key="`tag-${tag}`" v-text="tag" class="d-inline-flex fw-medium small py-2 px-3 border border-light full-radius me-2 bg-light"></div>
        </div>
        <div class="mb-3 mt-5 text-muted">
          <span v-html="`Since `+toString(post.date)"></span>
          <span>•</span>
          <span>{{reading_time}} minute read</span>
        </div>
      </div>
      <div id="article" class="mb-5">
        <nuxt-content :document="post" />
      </div>
      <a :href="`/projects/${post.slug}`" class="btn btn-outline-primary full-radius py-3 w-100">
        <span>Visit site</span>
        <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-arrow-narrow-right" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
          <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
          <line x1="5" y1="12" x2="19" y2="12"></line>
          <line x1="15" y1="16" x2="19" y2="12"></line>
          <line x1="15" y1="8" x2="19" y2="12"></line>
        </svg>
      </a>
    </div>
  </section>
</template>

<script>
export default {
  async asyncData({ $content, params, error }) {
    let post;
    try {
      post = await $content("project", params.slug).fetch();
      // OR const article = await $content(`articles/${params.slug}`).fetch()
    } catch (e) {
      error({ message: "Project Post not found" });
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
