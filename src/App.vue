<template>
  <div id="app">
    <Title msg="Something something"/>
  </div>
</template>

<script>
import Title from './components/Title.vue'

export default {
  name: 'app',
  components: {
    Title
  }
}
</script>

<style>
  #app {
  }
</style>
