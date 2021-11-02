<template>
  <section class="py-7 front-banner">
    <div class="container px-4">
      <h1>I'm Yanuar, a backend developer based in Yogyakarta, Indonesia. Specialized on creating awesome system ecosystems both web and mobile devices.</h1>
      <p class="lead">I am specialized in designing meaningful and intuitives systems for web and mobile devices. <br> Currently working at logistic aggregator startup
        <a href="//kiriminaja.com">KiriminAja</a>
      </p>
      <div class="mt-3">
        <nuxt-link to="/about" class="btn btn-lg btn-primary full-radius px-lg-4">
          About me
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M15.0378 6.34326L13.6269 7.76078L16.8972 11.0157L3.29211 11.0294L3.29413 13.0294L16.8619 13.0158L13.6467 16.246L15.0643 17.6569L20.7079 11.9869L15.0378 6.34326Z" fill="black"/>
          </svg>
        </nuxt-link>
        <nuxt-link to="/blogs" class="btn btn-lg btn-link full-radius px-lg-4">My Blogs</nuxt-link>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  head() {
    return {
      title: "Hometown",
      script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }],
    };
  },
}
</script>
