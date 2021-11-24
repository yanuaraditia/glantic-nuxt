<template>
  <section class="pb-7 pt-4">
    <div class="container px-3 px-lg-4">
      <img src="~/assets/my-team.png" class="img-fluid main-radius mt-5" alt="">
      <p class="mt-5 lead">Hi there! My name is <span class="fw-medium">Yanuar Aditia</span>, and Yanuar in short.</p>
      <p class="lead">Born, raised in <a href="//kebumenkab.go.id">Kebumen, Indonesia</a>. Currently living in <a href="//jogjaprov.go.id">Yogyakarta, Indonesia</a> and working as backend web dev work for a startup based
        <a href="//kiriminaja.com">KiriminAja</a> and finished my bachelor's degree in Informatics on Software Engineering at <a
          href="//amikom.ac.id">Universitas Amikom Yogyakarta</a>.
      </p>
      <p class="lead">I start getting into backend development on college by creating an internal dashboard/CMS for practicum management using CodeIgniter, then focused on it by working as a full-stack developer at
        <a href="//tries.co.id">Tries Indonesia</a>. From then until now, I am focused on backend development mostly on Laravel + MySQL + REST API codebases.
      </p>
      <p class="lead">Photo above is from my we-fie photo at <a href="//instagram.com/kiriminajacom">@kiriminajacom</a>.</p>
      <div class="my-5">
        <div class="row">
          <div class="col-6 col-lg-3">
            <h4>Languages</h4>
            <ul class="list-unstyled stratum">
              <li>CSS & HTML</li>
              <li>JavaScript</li>
              <li>TypeScript</li>
              <li>PHP</li>
            </ul>
          </div>
          <div class="col-6 col-lg-3">
            <h4>Frontend</h4>
            <ul class="list-unstyled stratum">
              <li>Bootstrap</li>
              <li>Bulma</li>
              <li>Next.js</li>
              <li>Nuxt.js</li>
              <li>Styled Components</li>
            </ul>
          </div>
          <div class="col-6 col-lg-3">
            <h4>Backend</h4>
            <ul class="list-unstyled stratum">
              <li>MySQL</li>
              <li>RestAPI</li>
              <li>Node.js</li>
              <li>Nginx</li>
            </ul>
          </div>
          <div class="col-6 col-lg-3">
            <h4>Tools of the trade</h4>
            <ul class="list-unstyled stratum">
              <li>PhpStorm</li>
              <li>Figma</li>
              <li>Git</li>
              <li>Postman</li>
              <li>WebStorm</li>
            </ul>
          </div>
          <div class="col-6 col-lg-3">
            <h4>Infrastructure</h4>
            <ul class="list-unstyled stratum">
              <li>Cloudflare</li>
              <li>Google Cloud Platform</li>
              <li>Amazon Web Services</li>
              <li>Netlify</li>
              <li>Vercel</li>
              <li>Github Workflows</li>
            </ul>
          </div>
        </div>
      </div>
      <p class="lead">You can reach out via email at <a href="mailto:me@yan.my.id">me@yan.my.id</a>, or via socials below:</p>
      <ul class="lead">
        <li>Github — <a href="//github.com/yanuaraditia">github.com/yanuaraditia</a></li>
        <li>Facebook — <a href="//facebook.com/yanuaraditia99">facebook.com/yanuaraditia99</a></li>
        <li>LinkedIn — <a href="//linkedin.com/in/yanuaraditia">linkedin.com/in/yanuaraditia</a></li>
      </ul>
    </div>
  </section>
</template>
<script>
export default {
  head() {
    return {
      title: "Me"
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
