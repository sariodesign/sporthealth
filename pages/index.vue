<template>
  <div>
    <Hero :typeHero='typeHero' />
    <MainCategories />
    <Methods />
  </div>
</template>
<script>
import Hero from '~/components/Hero.vue'
import MainCategories from '~/components/MainCategories.vue'
import Methods from '~/components/Methods.vue'

export default {
  components: {
    Hero,
    MainCategories,
    Methods
  },
  data(){
    return {
      typeHero: 'homepage'
    }
  }
}
</script>
