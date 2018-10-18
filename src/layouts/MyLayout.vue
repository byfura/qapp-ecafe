<template>
  <q-layout view="lHh Lpr lFf">
    <q-layout-header>
      <q-toolbar
        color="primary"
        :inverted="$q.theme === 'ios'"
      >
        <q-btn
          flat
          dense
          round
          @click="leftDrawerOpen = !leftDrawerOpen"
          aria-label="Menu"
        >
          <q-icon name="menu" />
        </q-btn>

        <q-toolbar-title>
          English Cafe  
        </q-toolbar-title>
      </q-toolbar>
    </q-layout-header>

    <q-layout-drawer
      v-model="leftDrawerOpen"
      :content-class="$q.theme === 'mat' ? 'bg-secondary' : null"
    >
      <q-list
        no-border
        link
        inset-delimiter
      >
        <q-list-header><span class="q-title">Menu</span></q-list-header>
        <q-item to="/">
          <q-item-side color="primary" icon="home" />
          <q-item-main label="Home" />
        </q-item>
        <q-item to="/lesson">
          <q-item-side color="primary" icon="school" />
          <q-item-main label="Lesson" />
        </q-item>
        <q-item to="/quiz">
          <q-item-side color="primary" icon="description" />
          <q-item-main label="Quiz"/>
        </q-item>
      </q-list>
    </q-layout-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { openURL } from 'quasar'

export default {
  name: 'MyLayout',
  data () {
    return {
      leftDrawerOpen: this.$q.platform.is.desktop
    }
  },
  methods: {
    openURL
  }
}
</script>

<style>
</style>
