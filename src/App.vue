<template>
  <!-- Don't drop "q-app" class -->
  <div id="q-app">
    <q-toolbar slot="header" class="toolbar">
        <img src="~assets/insurtech_logo.png">
      <div align="end">
      <q-btn flat><q-icon name="home"/>Home</q-btn>
      <q-btn flat><q-icon name="search"/>Search</q-btn>
      </div>
     <!-- <q-toolbar-title>
        InsurTech Lab
        <div slot="subtitle">Virtusa</div>
      </q-toolbar-title> -->
    </q-toolbar>
    <router-view class="layout-view"></router-view>
  </div>
</template>

<script>

import {
  QLayout,
  QToolbar,
  QToolbarTitle,
  QBtn,
  QIcon,
  QList,
  QListHeader,
  QItem,
  QItemSide,
  QItemMain
} from 'quasar'
/*
 * Root component
 */
export default {
  components: {
    QLayout,
    QToolbar,
    QToolbarTitle,
    QBtn,
    QIcon,
    QList,
    QListHeader,
    QItem,
    QItemSide,
    QItemMain
  }
}
</script>

<style></style>
