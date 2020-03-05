<template>
  <div>
    <Hero :typeHero='typeHero' />
    <MainCategories />
  </div>
</template>

<script>
import Hero from '~/components/Hero.vue'
import MainCategories from '~/components/MainCategories.vue'

export default {
  components: {
    Hero,
    MainCategories
  },
  data(){
    return {
      typeHero: 'homepage'
    }
  }
}
</script>
