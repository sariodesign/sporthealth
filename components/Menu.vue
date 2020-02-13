<template>
    <ul class="c-navigation__menu flex justify-between">
        <li>
          <nuxt-link class="c-navigation__link" to="/">Home</nuxt-link>
        </li>
        <li v-for="item in items">
            <nuxt-link class="c-navigation__link" :to=item.link>
                {{item.page}}
            </nuxt-link>
        </li>
    </ul>
</template>
<script>
export default {
  data () {
    return {
      items: [
        { page: 'Fisioterapia',
          link: '/fisioterapia'},
        { page: 'Osteopatia',
          link: '/osteopatia'},
        { page: 'Idrokinesiterapia',
          link: '/idrokinesiterapia'},
        { page: 'Riatletizzazione',
          link: '/riatletizzazione'},
        { page: 'Neuromotoria',
          link: 'neuromotoria'},
        { page: 'Consulenze',
          link: '/consulenze'},
        { page: 'Prodotti',
          link: 'prodotti'}
      ] 
    }
  }
}
</script>
