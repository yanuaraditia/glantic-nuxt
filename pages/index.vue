<template>
  <section class="py-7 front-banner">
    <div class="container px-3 px-lg-4 text-lg-center">
      <nuxt-link to="/about" class="full-radius d-inline-flex meee bg-primary bg-opacity-10 overflow-hidden">
        <img src="~/assets/funny-boy.png" alt="" style="max-width: 350px">
      </nuxt-link>
      <h1 class="mt-3">Hey! I'm Yanuar Aditia.</h1>
      <div class="mx-auto px-lg-5" style="max-width: 1200px">
        <p class="lead">I am specialized in designing meaningful and intuitives systems for web and mobile devices. <br> Currently working at logistic aggregator startup
          <a href="//kiriminaja.com">KiriminAja</a>
        </p>
      </div>
      <div class="mt-3">
        <nuxt-link to="/about" class="btn btn-lg btn-primary bg-primary text-light border-0 bg-opacity-10 full-radius px-lg-4">
          About me
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M15.0378 6.34326L13.6269 7.76078L16.8972 11.0157L3.29211 11.0294L3.29413 13.0294L16.8619 13.0158L13.6467 16.246L15.0643 17.6569L20.7079 11.9869L15.0378 6.34326Z" fill="currentColor"/>
          </svg>
        </nuxt-link>
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
<style lang="scss" scoped>
.meee {
  img {
    transition: all .2s ease-in-out;
  }
  &:hover {
    img {
      transform: scale(1.15) translateY(20px) rotate(-2deg);
    }
  }
}
</style>
