<template>
  <q-layout view="hHh lpR fff">
    <q-header>
      <q-toolbar class="bg-primary text-blue-grey-9 nav-bar">
        <q-avatar
          class="q-ml-sm">
          <img src="statics/hero.jpeg">
        </q-avatar>

        <q-toolbar-title class="text-weight-bold">
          <span class="hero-name">
            carlos-tovar.me
          </span>
        </q-toolbar-title>

        <q-separator dark vertical />
        <nav-button
          href="https://github.com/cartovarc">
          Github
        </nav-button>
        <q-separator dark vertical />
        <nav-button
          href="https://www.linkedin.com/in/carlos-fernando-tovar-ceron">
          Linkedin
        </nav-button>
      </q-toolbar>
    </q-header>

    <q-page-container>
        <router-view />
    </q-page-container>

    <q-footer>
      <q-toolbar>
        <q-toolbar-title
          class="footer q-ml-lg q-mr-lg text-subtitle1">
          Copyright © 2020 Carlos Tovar
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>

<script>
import EssentialLink from 'components/EssentialLink'

export default {
  name: 'MainLayout',

  components: {
    'nav-button': require("components/NavButton.vue").default
  },

  data () {
    return {
      leftDrawerOpen: false,
      essentialLinks: [
        {
          title: 'Docs',
          caption: 'quasar.dev',
          icon: 'school',
          link: 'https://quasar.dev'
        }
      ]
    }
  }
}
</script>

<style>
  .nav-bar {
    height: 3.6rem;
    border-bottom: 1px solid;
    border-bottom-color: rgb(234, 236, 239);
  }
  .footer {
    padding: 2.5rem;
    border-top: 1px solid #eaecef;
    text-align: center;
    color: #4e6e8e;
  }
</style>
