<template>
  <q-card class="my-card">
    <q-img :src="img" />

    <q-card-section>
      <q-btn
        fab
        color="blue-grey-9"
        icon="event"
        class="absolute no-pointer-events"
        style="top: 0; right: 12px; transform: translateY(-50%);"
      />

      <div class="row no-wrap items-center">
        <div class="col text-h6 ellipsis text-blue-grey-9">{{ title }}</div>
      </div>

      <q-linear-progress size="25px" :value="progress" color="blue-grey-9">
        <div class="absolute-full flex flex-center">
          <q-badge color="white" text-color="blue-grey-9" :label="progressLabel1" />
        </div>
      </q-linear-progress>
    </q-card-section>

    <q-card-section class="q-pt-none">
      <div class="text-caption" style="color: #4e6e8e;">{{ description }}</div>
    </q-card-section>

    <q-separator />

    <q-card-actions align="right">
      <project-button icon="visibility" :href="demo">Demo</project-button>
      <project-button icon="code" :href="github">Code</project-button>
    </q-card-actions>
  </q-card>
</template>

<script>
export default {
  props: ["title", "description", "progress", "img", "github", "demo"],
  computed: {
    progressLabel1() {
      return (this.progress * 100).toFixed(2) + "%";
    }
  },
  components: {
    "project-button": require("components/ProjectButton.vue").default
  }
};
</script>

<style scoped>
.my-card {
  min-width: 260px;
}
</style>