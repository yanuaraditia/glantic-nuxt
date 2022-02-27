<template>
  <section class="py-7 pb-lg-2 front-banner">
    <div class="cupertino"></div>
    <div class="container px-3 px-lg-4 text-lg-center">
      <nuxt-link to="/about" class="full-radius d-inline-flex meee overflow-hidden">
        <img src="~/assets/me.jpg" alt="darth vader" style="max-width: 210px">
      </nuxt-link>
      <h1 class="mt-3 h1">Halo! I'm Yanuar Aditia.</h1>
      <div class="mx-auto px-lg-5" style="max-width: 700px">
        <p class="lead">Software engineer at logistic technology startup
          <a href="//kiriminaja.com">KiriminAja</a>. Lives in Yogyakarta, Indonesia.
        </p>
      </div>
      <div class="row g-3 justify-lg-content-center">
        <div class="col-auto">
          <a href="//linkedin.com/in/yanuaraditia" class="bg-primary bg-opacity-10 p-2 full-radius d-inline-flex">
            <svg xmlns="http://www.w3.org/2000/svg" class="icon" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="currentColor" fill-opacity="0.2" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><rect x="4" y="4" width="16" height="16" rx="2" /><line x1="8" y1="11" x2="8" y2="16" /><line x1="8" y1="8" x2="8" y2="8.01" /><line x1="12" y1="16" x2="12" y2="11" /><path d="M16 16v-3a2 2 0 0 0 -4 0" /></svg>
          </a>
        </div>
        <div class="col-auto">
          <a href="//github.com/yanuaraditia" class="bg-primary bg-opacity-10 p-2 full-radius d-inline-flex">
            <svg xmlns="http://www.w3.org/2000/svg" class="icon" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="currentColor" fill-opacity="0.2" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M9 19c-4.3 1.4 -4.3 -2.5 -6 -3m12 5v-3.5c0 -1 .1 -1.4 -.5 -2c2.8 -.3 5.5 -1.4 5.5 -6a4.6 4.6 0 0 0 -1.3 -3.2a4.2 4.2 0 0 0 -.1 -3.2s-1.1 -.3 -3.5 1.3a12.3 12.3 0 0 0 -6.2 0c-2.4 -1.6 -3.5 -1.3 -3.5 -1.3a4.2 4.2 0 0 0 -.1 3.2a4.6 4.6 0 0 0 -1.3 3.2c0 4.6 2.7 5.7 5.5 6c-.6 .6 -.6 1.2 -.5 2v3.5" /></svg>
          </a>
        </div>
        <div class="col-auto">
          <a href="//gitlab.com/ngal0r" class="bg-primary bg-opacity-10 p-2 full-radius d-inline-flex">
            <svg xmlns="http://www.w3.org/2000/svg" class="icon" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="currentColor" fill-opacity="0.2" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M21 14l-9 7l-9 -7l3 -11l3 7h6l3 -7z" /></svg>
          </a>
        </div>
        <div class="col-auto">
          <a href="//twitter.com/yanuaraditiaa" class="bg-primary bg-opacity-10 p-2 full-radius d-inline-flex">
            <svg xmlns="http://www.w3.org/2000/svg" class="icon" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="currentColor" fill-opacity="0.2" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M22 4.01c-1 .49 -1.98 .689 -3 .99c-1.121 -1.265 -2.783 -1.335 -4.38 -.737s-2.643 2.06 -2.62 3.737v1c-3.245 .083 -6.135 -1.395 -8 -4c0 0 -4.182 7.433 4 11c-1.872 1.247 -3.739 2.088 -6 2c3.308 1.803 6.913 2.423 10.034 1.517c3.58 -1.04 6.522 -3.723 7.651 -7.742a13.84 13.84 0 0 0 .497 -3.753c-.002 -.249 1.51 -2.772 1.818 -4.013z" /></svg>
          </a>
        </div>
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
