<template>
  <section class="py-7 reader-section">
    <div class="container px-3 px-lg-4 pt-xl-6">
      <h1 class="h1">Contact Me</h1>
      <p class="lead text-muted">Here's how to reach me, looking forward to talk with y'all!</p>
      <div class="mt-5 mt-lg-8">
        <p class="lead">Inquiries via email at <a href="mailto:yanuar@kiriminaja.com">yanuar@kiriminaja.com</a> or via socials below:</p>
        <ul class="lead">
          <li class="mb-3">GitHub - <a href="//github.com/yanuaraditia">https://github.com/yanuaraditia</a></li>
          <li class="mb-3">LinkedIn - <a href="//linkedin.com/in/yanuaraditia">https://linkedin.com/in/yanuaraditia</a></li>
          <li class="mb-3">Telegram - <a href="//t.me/yanuaraditia">https://t.me/yanuaraditia</a></li>
        </ul>
        <p class="lead mb-5">View my resume online via <a href="https://resume.io/r/jEMSdeCkn">resume.io</a>.</p>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  head() {
    return {
      title: "Contact Me"
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
