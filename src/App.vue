<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png">
    <contenu></contenu>
  </div>
</template>

<script>

import Contenu from './components/Contenu-name.vue'

export default {
  name: 'App',
  components: {
    'contenu': Contenu
  }
}
</script>

<style>

</style>
