<template>
  <section class="py-7 reader-section">
    <div class="container px-3 px-lg-4 pt-xl-6">
      <h1>Creations and projects</h1>
      <p class="lead text-muted">Here are some of my past works from personal projects and open source ones.</p>
      <div class="mt-5">
        <div class="project row g-3">
          <div class="project-item col-lg-6 mb-3" v-for="project of projects" :key="project.slug">
            <div class="link-top card bg-transparent border-0 overflow-hidden main-radius">
              <div class="top-img bg-primary overflow-hidden bg-opacity-10 main-radius">
                <img :src="project.img" alt="" style="transform: translateX(1rem) translateY(1rem)">
              </div>
              <div class="card-body p-lg-4 align-items-center d-flex">
                <div class="w-100">
                  <h4 class="card-title h5" v-html="project.title"></h4>
                  <p class="card-text" v-html="project.description"></p>
                  <div class="text-primary mb-2">
                    <span>Visit website</span>
                    <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-arrow-narrow-right" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                      <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
                      <line x1="5" y1="12" x2="19" y2="12"></line>
                      <line x1="15" y1="16" x2="19" y2="12"></line>
                      <line x1="15" y1="8" x2="19" y2="12"></line>
                    </svg>
                  </div>
                  <span v-for="tag in project.tags" v-html="tag" class="badge bg-light bg-opacity-25 me-1"></span>
                </div>
              </div>
              <a :href="project.url"></a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const projects = await $content("project")
      .sortBy('created_at','desc')
      .fetch();

    return {
      projects,
    };
  },
  methods: {
    toString(date) {
      const options = { year: 'numeric', month: 'long', day: 'numeric' }
      return new Date(date).toLocaleDateString('id', options)
    }
  },
  head() {
    return {
      title: "Creations and projects"
    }
  }
};
</script>

<style lang="scss">
.project {
  &-list {
    position: relative;
    &:not(:hover) {
      .card-body {
        opacity: 0;
        pointer-events: none;
      }
    }
    .card-body {
      transition: all .2s ease-in-out;
      background: rgba(#000, .75);
      backdrop-filter: blur(5px);
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      top: 0;
    }
  }
}
</style>
