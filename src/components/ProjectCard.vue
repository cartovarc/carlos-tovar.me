<template>
    <q-card class="my-card">
      <q-img :src="img" />

      <q-card-section>
        <q-btn
          fab
          color="blue-grey-9"
          icon="event"
          class="absolute"
          style="top: 0; right: 12px; transform: translateY(-50%);"
        />

        <div class="row no-wrap items-center">
          <div class="col text-h6 ellipsis text-blue-grey-9">
            {{ title }}
          </div>
        </div>

        <q-rating
          readonly
          v-model="stars"
          :max="5"
          size="3em"
          color="blue"
          :icon="icons"
        />

      </q-card-section>

      <q-card-section class="q-pt-none">
        <div
          class="text-caption"
          style="color: #4e6e8e;">
          {{ description }}
        </div>
      </q-card-section>

      <q-separator />

      <q-card-actions align="right">
        <project-button
          icon="visibility"
          :href="demo">
          Demo
        </project-button>
        <project-button
          icon="code"
          :href="github">
          Code
        </project-button>
      </q-card-actions>
    </q-card>

</template>

<script>
export default {
  props: ['title', 'description', 'stars', "img", 'github', 'demo'],
  data () {
    return {
      icons: [
        'sentiment_very_dissatisfied',
        'sentiment_dissatisfied',
        'sentiment_neutral',
        'sentiment_satisfied',
        'sentiment_very_satisfied'
      ]
    }
  },
  components: {
    'project-button': require('components/ProjectButton.vue').default,
  }
}
</script>
