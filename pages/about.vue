<template>
  <section class="py-7 reader-section">
    <div class="container px-3 px-lg-4 pt-xl-6">
      <img src="~/assets/teams/wefie-photos.png" class="img-fluid w-100 mt-3" alt="">
      <p class="lead mt-3 mb-5 fw-medium text-muted">Hi there! My name is <span class="fw-medium">Yanuar Aditia</span>, and Yanuar in short.</p>
      <h1 class="h4">About Myself</h1>
      <p class="lead">I am a software engineer specialized in backend development, creating web based applications from management system and core engine, to monolith and micro-services.</p>
      <p class="lead">Born and raised in 🇮🇩 Kebumen, Indonesia. Currently based on Yogyakarta, Indonesia. Majored my bachelor's degree on Informatics at
        <a href="//amikom.ac.id">Universitas Amikom Yogyakarta</a> on 2019. Currently work as a Development Lead on <a
          href="//kiriminaja.com">KiriminAja</a>. Previously doing full-stack development on <a href="//tries.co.id">Tries Digital Indonesia</a>.
      </p>
      <p class="lead">Started programming on backend development creating an internal management system for my company project using
        <a href="//laravel.org">Laravel</a> and <a href="https://voyager.devdojo.com/">Voyager</a>. After 11 month I decide to work on new team as backend developer, which then focusing on project management and continue develop with until present day.</p>
      <p class="lead mb-5">View my resume online via <a href="https://resume.io/r/jEMSdeCkn">resume.io</a>. Head over to my <nuxt-link to="contact">contact page</nuxt-link> to reach out.</p>
      <h4>Work Experience</h4>
      <ul class="lead mb-5">
        <li class="mb-1">Development Lead at <a href="//kiriminaja.com">KiriminAja</a> (April 2022 - present)</li>
        <li class="mb-1">Backend Engineer at KiriminAja (May 2021 - March 2022)</li>
        <li class="mb-1">Full-Stack Developer at KiriminAja (November 2020 - May 2021)</li>
        <li class="mb-1">Full-Stack Developer at TRIES (February 2020 - November 2020)</li>
        <li class="mb-1">Laboratory Assistant at Universitas Amikom Yogyakarta (September 2018 - January 2019)</li>
      </ul>
      <h4>Currently Using</h4>
      <ul class="lead mb-5">
        <li class="mb-1"><strong>Notebook:</strong> <a href="https://www.apple.com/id/macbook-pro-13/">MacBook Pro 2020</a> +
          <a href="https://www.apple.com/id/macos/monterey/">MacOS Monterey</a></li>
        <li class="mb-1"><strong>Hosting:</strong> <a href="https://cloud.google.com/">Google Cloud</a>, <a href="https://www.netlify.com/">Netlify</a>, <a href="https://vercel.com/">Vercel</a></li>
        <li class="mb-1"><strong>IDE:</strong> <a href="https://www.jetbrains.com/phpstorm/">PHPStorm</a>, <a
          href="https://www.jetbrains.com/webstorm/">WebStorm</a>, <a href="https://www.jetbrains.com/datagrip/">DataGrip</a></li>
        <li class="mb-1"><strong>Management:</strong> <a href="https://www.atlassian.com/software/jira">Jira Software</a>,
          <a href="https://www.atlassian.com/software/confluence">Confluence</a></li>
      </ul>
      <p class="lead">Read more about my experiences on <a href="//linked.in/in/yanuaraditia">LinkedIn</a></p>
    </div>
  </section>
</template>
<script>
export default {
  head() {
    return {
      title: "About Me"
    }
  }
}
</script>
<style scoped lang="scss">
.stratum {
  margin-top: .5rem;
  li {
    &:not(:last-child) {
      margin-bottom: .5rem;
    }
    font-weight: 500;
  }
}
</style>
