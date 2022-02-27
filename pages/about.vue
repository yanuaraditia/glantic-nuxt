<template>
  <section class="pb-7 pt-0">
    <div class="container px-3 px-lg-4">
      <img src="~/assets/teams/townhall.jpg" class="img-fluid w-100 main-radius mt-3" alt="">
      <div class="py-2 mt-4">
        <h1>Bigger Better Faster</h1>
      </div>
      <p class="lead">Hi there! My name is <span class="fw-medium">Yanuar Aditia</span>, and Yanuar in short.</p>
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
            <div class="card" v-bind:class="[($nuxt.$colorMode.preference === 'dark' ? 'bg-dark' : 'bg-light')]">
              <div class="card-body p-lg-4">
                <h4 class="h5">Languages</h4>
                <ul class="ps-3 stratum m-0">
                  <li>PHP</li>
                  <li>CSS</li>
                  <li>HTML</li>
                  <li>JavaScript</li>
                </ul>
              </div>
            </div>
          </div>
          <div class="col-6 col-lg-3">
            <div class="card" v-bind:class="[($nuxt.$colorMode.preference === 'dark' ? 'bg-dark' : 'bg-light')]">
              <div class="card-body p-lg-4">
                <h4 class="h5">Backend</h4>
                <ul class="ps-3 stratum m-0">
                  <li>Laravel</li>
                  <li>MySQL</li>
                  <li>RestAPI</li>
                  <li>Node.js</li>
                </ul>
              </div>
            </div>
          </div>
          <div class="col-6 col-lg-3">
            <div class="card" v-bind:class="[($nuxt.$colorMode.preference === 'dark' ? 'bg-dark' : 'bg-light')]">
              <div class="card-body p-lg-4">
                <h4 class="h5">Tools of the trade</h4>
                <ul class="ps-3 stratum m-0">
                  <li>PhpStorm</li>
                  <li>Jira & Confluence</li>
                  <li>Git</li>
                  <li>Insomnia</li>
                </ul>
              </div>
            </div>
          </div>
          <div class="col-6 col-lg-3">
            <div class="card" v-bind:class="[($nuxt.$colorMode.preference === 'dark' ? 'bg-dark' : 'bg-light')]">
              <div class="card-body p-lg-4">
                <h4 class="h5">Front-End</h4>
                <ul class="ps-3 stratum m-0">
                  <li>Bootstrap</li>
                  <li>Nuxt.js</li>
                  <li>Styled Components</li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
      <p class="lead">You can reach out via email at <a href="mailto:yanuar@kiriminaja.com">yanuar@kiriminaja.com</a>, or via socials below:</p>
      <ul class="lead">
        <li>Twitter — <a href="//twitter.com/yanuaraditiaa">twitter.com/yanuaraditiaa</a></li>
        <li>Telegram — <a href="//t.me/yanuaraditia">t.me/yanuaraditia</a></li>
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
