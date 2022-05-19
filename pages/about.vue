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
        <li class="mb-1">Development Lead at <a href="//kiriminaja.com" class="fw-medium">KiriminAja</a> <small class="text-muted" style="font-size: .75rem">(Apr 2022 - present)</small></li>
        <li class="mb-1">Backend Engineer at <a href="//kiriminaja.com" class="fw-medium">KiriminAja</a> <small class="text-muted" style="font-size: .75rem">(May 2021 - Mar 2022)</small></li>
        <li class="mb-1">Full-Stack Developer at <a href="//kiriminaja.com" class="fw-medium">KiriminAja</a> <small class="text-muted" style="font-size: .75rem">(Nov 2020 - May 2021)</small></li>
        <li class="mb-1">Full-Stack Developer at <a href="//tries.co.id" class="fw-medium">Tries Digital Indonesia</a> <small class="text-muted" style="font-size: .75rem">(Feb 2020 - Nov 2020)</small></li>
        <li class="mb-1">Laboratory Assistant at Universitas Amikom Yogyakarta <small class="text-muted" style="font-size: .75rem">(Sep 2018 - Jan 2019)</small></li>
      </ul>
      <h4>Hardware</h4>
      <ul class="lead mb-5">
        <li class="mb-1"><span class="fw-medium">Coding PC:</span> <a href="https://www.apple.com/id/macbook-pro-13/">M1 MacBook Pro 13" 2020</a></li>
        <li class="mb-1"><span class="fw-medium">Phone:</span> <a href="https://www.mi.co.id/id/product/redmi-note-10/">Redmi Note 10</a></li>
        <li class="mb-1"><span class="fw-medium">Earphone:</span> <a href="http://www.eggeltech.com/home/24-eggel-energy-buds-pro.html">Eggel Energy Buds Pro</a></li>
      </ul>
      <h4>Tools</h4>
      <ul class="lead mb-5">
        <li class="mb-1">This website is hosted on <a href="//netlify.com">Netlify</a> and uses the <a href="//nuxtjs.org">Nuxt</a> framework</li>
        <li class="mb-1"><span class="fw-medium">Coding:</span> <a href="//jetbrains.com">JetBrains Family</a></li>
        <li class="mb-1"><span class="fw-medium">Terminal:</span> <a href="https://support.apple.com/en-gb/guide/terminal/welcome/mac">Mac Terminal</a></li>
        <li class="mb-1"><span class="fw-medium">Notes:</span> <a href="https://www.atlassian.com/software/confluence">Confluence</a></li>
        <li class="mb-1"><span class="fw-medium">Task Management:</span> <a href="https://www.atlassian.com/software/jira">Jira</a></li>
        <li class="mb-1"><span class="fw-medium">Music:</span> <a href="//spotify.com">Spotify</a>
          <iframe class="main-radius mt-2" src="https://open.spotify.com/embed/track/5n8YOy9hd8o4d3OHteTVCJ?utm_source=generator&theme=0" width="100%" height="80" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"></iframe>
        </li>
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
