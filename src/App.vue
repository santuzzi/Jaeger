<template>
  <div id="app">
    <JaegerGallery/>
  </div>
</template>

<script>
import JaegerGallery from './components/JaegerGallery.vue'

export default {
  name: 'app',
  components: {
    JaegerGallery
  }
}
</script>

<style>
   body {
      font-family: "Open Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
      margin: 0;
      padding: 50px 0 0;
    }
</style>
