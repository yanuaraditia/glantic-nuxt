<template>
  <section class="py-7 pb-lg-2 front-banner">
    <div class="cupertino"></div>
    <div class="container px-3 px-lg-4 pt-xl-6 text-center">
      <nuxt-link to="/about" class="full-radius d-inline-flex bg-gradient bg-opacity-10 overflow-hidden">
        <div class="bg-dark bg-opacity-10">
          <img src="~/assets/8d60c665c4cfe35a91c79ef99bff8f31-sticker.png" alt="darth vader" style="max-width: 16rem; transform: scale(1.1)">
        </div>
      </nuxt-link>
      <h1 class="mt-3 h1">Halo! I'm Yanuar Aditia.</h1>
      <div class="mx-auto px-lg-5" style="max-width: 700px">
        <p class="lead">Development Lead at logistic technology startup
          <a href="//kiriminaja.com">KiriminAja</a>. Lives in Yogyakarta, Indonesia.
        </p>
      </div>
      <div class="row g-3 justify-content-center">
        <div class="col-auto">
          <a href="//t.me/yanuaraditia" title="Telegram" class="bg-primary bg-opacity-10 p-2 full-radius d-inline-flex">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M20 6.75C21.5188 6.75 22.75 5.51878 22.75 4C22.75 2.48122 21.5188 1.25 20 1.25C18.4812 1.25 17.25 2.48122 17.25 4C17.25 5.51878 18.4812 6.75 20 6.75Z" fill="currentColor"/>
              <path d="M19.04 8.15C17.47 7.81 16.19 6.53 15.85 4.96C15.72 4.35 15.71 3.76 15.82 3.2C15.95 2.58 15.49 2 14.85 2H7C4.24 2 2 4.24 2 7V13.95C2 16.71 4.24 18.95 7 18.95H8.5C8.78 18.95 9.14 19.13 9.3 19.35L10.8 21.34C11.46 22.22 12.54 22.22 13.2 21.34L14.7 19.35C14.89 19.1 15.18 18.95 15.5 18.95H17.01C19.77 18.95 22 16.72 22 13.96V9.15C22 8.52 21.42 8.06 20.8 8.18C20.24 8.28 19.65 8.28 19.04 8.15ZM8 12C7.44 12 7 11.55 7 11C7 10.45 7.44 10 8 10C8.55 10 9 10.45 9 11C9 11.55 8.56 12 8 12ZM12 12C11.44 12 11 11.55 11 11C11 10.45 11.44 10 12 10C12.55 10 13 10.45 13 11C13 11.55 12.56 12 12 12ZM16 12C15.44 12 15 11.55 15 11C15 10.45 15.44 10 16 10C16.55 10 17 10.45 17 11C17 11.55 16.56 12 16 12Z" fill="currentColor"/>
            </svg>
          </a>
        </div>
        <div class="col-auto">
          <a href="mailto:yanuaraditia@outlook.com" class="bg-primary bg-opacity-10 p-2 full-radius d-inline-flex">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M16.1391 2.95907L7.10914 5.95907C1.03914 7.98907 1.03914 11.2991 7.10914 13.3191L9.78914 14.2091L10.6791 16.8891C12.6991 22.9591 16.0191 22.9591 18.0391 16.8891L21.0491 7.86907C22.3891 3.81907 20.1891 1.60907 16.1391 2.95907ZM16.4591 8.33907L12.6591 12.1591C12.5091 12.3091 12.3191 12.3791 12.1291 12.3791C11.9391 12.3791 11.7491 12.3091 11.5991 12.1591C11.3091 11.8691 11.3091 11.3891 11.5991 11.0991L15.3991 7.27907C15.6891 6.98907 16.1691 6.98907 16.4591 7.27907C16.7491 7.56907 16.7491 8.04907 16.4591 8.33907Z" fill="currentColor"/>
            </svg>
          </a>
        </div>
        <div class="col-auto">
          <a href="//github.com/yanuaraditia" class="bg-primary bg-opacity-10 p-2 full-radius d-inline-flex">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M16.19 2H7.81C4.17 2 2 4.17 2 7.81V16.18C2 19.83 4.17 22 7.81 22H16.18C19.82 22 21.99 19.83 21.99 16.19V7.81C22 4.17 19.83 2 16.19 2ZM9.85 16.45C9.85 17.58 8.93 18.5 7.8 18.5C6.67 18.5 5.75 17.58 5.75 16.45C5.75 15.58 6.29 14.85 7.05 14.55V10.26C6.21 9.95 5.6 9.15 5.6 8.2C5.6 6.99 6.59 6 7.8 6C9.01 6 10 6.99 10 8.2C10 9.15 9.39 9.95 8.55 10.26V14.55C9.31 14.85 9.85 15.59 9.85 16.45ZM16.75 18.5C15.62 18.5 14.7 17.58 14.7 16.45C14.7 15.58 15.24 14.85 16 14.55V8.75C16 8.61 15.89 8.5 15.75 8.5H14.62L14.83 8.67C15.15 8.94 15.19 9.41 14.93 9.73C14.78 9.91 14.56 10 14.35 10C14.18 10 14.01 9.94 13.87 9.83L12.07 8.33C11.9 8.18 11.8 7.97 11.8 7.75C11.8 7.53 11.9 7.32 12.07 7.17L13.87 5.67C14.19 5.41 14.66 5.45 14.93 5.77C15.2 6.09 15.15 6.56 14.83 6.83L14.62 7H15.75C16.71 7 17.5 7.79 17.5 8.75V14.55C18.26 14.85 18.8 15.59 18.8 16.45C18.8 17.58 17.88 18.5 16.75 18.5Z" fill="currentColor"/>
            </svg>
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
