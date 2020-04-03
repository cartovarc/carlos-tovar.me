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
                          <q-img src="statics/hero.jpeg" :ratio="1" />
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
