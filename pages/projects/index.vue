<template>
  <section class="py-7">
    <div class="container px-3 px-lg-4">
      <h1>Creations and projects</h1>
      <p class="lead">Here are some of my past works from personal projects and open source ones.</p>
      <div class="mt-5">
        <div class="row project g-3">
          <div class="col-lg-6" v-for="project of projects" :key="project.slug">
            <div class="link-top card project-list border-0 overflow-hidden main-radius">
              <img :src="project.img" alt="">
              <div class="card-body text-white p-lg-4 text-lg-center align-items-center d-flex">
                <div class="w-100">
                  <h4 class="card-title" v-html="project.title"></h4>
                  <p class="card-text" v-html="project.description"></p>
                  <div class="text-primary mb-2">
                    <span v-html="project.url_text"></span>
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
