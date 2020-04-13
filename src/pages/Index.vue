<template>
  <div class="flex flex-center">
    <q-parallax
      class="q-mt-sm"
      src="statics/playa.jpg"
    >
      <div class="trees">
          <div class="row" style="min-height: 400px; width: 100%; padding: 24px;">
              <div id="parent" class="full-width row justify-center">
                  <div
                    class="col-8 self-center"
                    style="max-width: 280px;">
                      <q-avatar
                        class="q-mb-lg q-mt-sm"
                        style="width: 100%; height: 100%;">
                          <q-img src="https://avatars1.githubusercontent.com/u/26529546?s=460&u=7d9794f9b38aef28063e43bb92a70076eefbc5ae&v=4" :ratio="1" />
                      </q-avatar>
                  </div>
                  <div
                    class="col-12"
                    style="text-align: center;">
                      <p class="text-h3 text-weight-bold text-white">
                        Carlos <span class="text-red">Tovar</span>
                      </p>

                      <p class="text-h5 text-white">
                        <q-icon
                          class="justify vertical-middle"
                          name="computer"/>
                          <span class="text-white">
                            Fullstack developer
                          </span>
                      </p>
                  </div>
                  <div
                    class="col-11 self-center bg-grey-6"
                    style="overflow: auto;">
                  </div>
              </div>
          </div>
      </div>
    </q-parallax>
    <div class="q-pl-xl q-pt-lg">
      <q-separator class="q-mb-lg" />
      <div class="row">
        <div class="col-md-4 col-sm-12">
            <span class="text-h5 text-blue-grey-9">
              🔧 Easy to setup
            </span>
            <p
              style="max-width: 60%"
              class="q-mt-sm feature">
              Minimal setup, helps you focus on writing amazing code.
            </p>
        </div>

        <div class="col-md-4 col-sm-12">
            <span class="text-h5 text-blue-grey-9 ">
              ⚡️ Performant
            </span>
            <p
              style="max-width: 60%"
              class="q-mt-sm feature">
              Generates optimized, fast and awesome applications using cool frameworks.
            </p>
        </div>

        <div class="col-md-4 col-sm-12">
            <span class="text-h5 text-blue-grey-9">
              🚀 Cross platform
            </span>
            <p
              style="max-width: 60%"
              class="q-mt-sm feature">Creates mobile, web, and desktop applications.</p>
        </div>
      </div>
      <q-separator class="q-mt-lg" />
    </div>

    <div class="row">
      <div class="text-weight-bold text-center text-blue-grey-9 col-12 text-h4 q-mt-lg">
        My awesome projects
      </div>
      <q-carousel
          v-model="slide"
          swipeable
          animated
          :control-type="controlType"
          control-color="blue"
          navigation
          padding
          arrows
          height="520px"
          class="text-blue rounded-borders col-12"
        >
          <q-carousel-slide name="style" class="column no-wrap flex-center">
            <project-card
              title="awesome-todo"
              description="Stay organized and get more done with this awesome todo app"
              img="https://blogs.iadb.org/conocimiento-abierto/wp-content/uploads/sites/10/2016/09/Task-Management1.jpg"
              github="https://github.com/cartovarc/vuejs-playground/tree/master/quasarframework/awesome-todo"
              demo="https://cartovarc-awesome-todo.web.app/"
              :stars="3"/>
          </q-carousel-slide>
        </q-carousel>

    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      controlType: 'flat',
      controlTypeOptions: [
        { value: 'regular', label: 'regular' },
        { value: 'unelevated', label: 'unelevated' },
        { value: 'flat', label: 'flat (default)' },
        { value: 'outline', label: 'outline' },
        { value: 'push', label: 'push' }
      ],
      slide: 'style',
      lorem: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo.'
    }
  },
  components: {
    'project-card': require('components/ProjectCard.vue').default,
  }
}
</script>

<style lang="scss">
  @media screen and (max-width: 768px){
    .hero-name  {
      display: none;
    }
  }

  .q-parallax__content {
    background-color: rgba(0,0,0,.6) !important;
  }

  .feature {
    color: #4e6e8e;
  }

</style>
