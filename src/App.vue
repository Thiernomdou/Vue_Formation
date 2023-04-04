<template>
  <div>
    <contenu></contenu>
    <header-top></header-top>
  </div>
</template>

<script>

import Contenu from './components/Contenu-name.vue'
import Header from './components/Header-top.vue'

export default {
  name: 'App',
  components: {
    'contenu': Contenu,
    'header-top': Header
  }
}
</script>

<style>

</style>
