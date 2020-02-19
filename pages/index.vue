<template>
  <div>
    <Navigation />
    <MainCategories />
    <Methods />
  </div>
</template>
<script>
  import MainCategories from '~/components/MainCategories.vue'
  import Methods from '~/components/Methods.vue'
    
  export default {
    components: {
      MainCategories,
      Methods
    }
  }
</script>
