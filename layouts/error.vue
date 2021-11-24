<template>
  <section>
    <div class="error text-center py-lg-5">
      <div class="text-muted mb-8">
        <img src="~/assets/monkey.png" style="max-width: 400px" class="img-fluid" alt="">
      </div>
      <h3 class="h2 title">{{ message }}</h3>
      <div v-if="statusCode === 404" class="description mx-lg-5 px-lg-5">
        <p class="mx-auto lead" style="max-width: 700px">URL yang kamu maksud salah. Coba cek lagi deh, disini hanya ada aku yang tak pernah kau anggap 😢</p>
        <a v-if="typeof $route === 'undefined'" class="error-link" href="/"></a>
        <NuxtLink v-else class="btn btn-primary bg-primary bg-opacity-10 border-0 text-white mt-4 full-radius btn-lg" to="/">Bring Me to Life</NuxtLink>
      </div>
      <p class="mx-auto lead" style="max-width: 700px" v-else>An error occurred while rendering the page. Check developer tools console for details.</p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'NuxtError',
  props: {
    error: {
      type: Object,
      default: null
    }
  },
  computed: {
    statusCode () {
      return (this.error && this.error.statusCode) || 500
    },
    message () {
      return this.error.message || 'Error'
    }
  },
  head () {
    return {
      title: this.message,
      meta: [
        {
          name: 'viewport',
          content: 'width=device-width,initial-scale=1.0,minimum-scale=1.0'
        }
      ]
    }
  }
}
</script>
