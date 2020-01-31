<template>
  <div class="wrapper">
    <Navigation />
    <nuxt />
  </div>
</template>
<script>
import Navigation from '~/components/Navigation.vue'

export default {
  components: {
    Navigation
  }
}
</script>
