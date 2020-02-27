<template>
    <ul class="c-navigation__menu flex justify-between">
        <li>
          <nuxt-link class="c-navigation__link" to="/">
            <img src="logo-sporthealth-menu.png"/>
          </nuxt-link>
        </li>
        <li class="c-navigation__item" v-for="item in items" :key="item.id">
            <nuxt-link class="c-navigation__link" :to=item.link>
                {{item.page}}
            </nuxt-link>
            <div v-if="item.submenu">
              <div class="c-navigation__toggle-submenu" :class="{'is-active' : isExpand}" @click="openSubmenu()"></div>
              <ul class="c-navigation__submenu" :class="{'is-expanded' : isExpand}">
                <li class="c-navigation__subitem" v-for="subitem in item.submenu">
                  <nuxt-link class="c-navigation__link" :to=subitem.link>
                    {{subitem.page}}
                  </nuxt-link>
                </li>
              </ul>
            </div>
        </li>
    </ul>
</template>
<script>
export default {
  data () {
    return {
      items: [
        { page: 'Fisioterapia',
          link: '/fisioterapia',
          submenu: [
            {
              page: 'Massoterapia',
              link: '/massoterapia'
            },
            {
              page: 'Rieducazione posturale',
              link: '/rieducazione-posturale'
            },
            {
              page: 'Pavimento pelvico',
              link: '/pavimento-pelvico'
            },
            {
              page: 'Tecarterapia',
              link: '/tecarterapia'
            },
            {
              page: 'Laserterapia',
              link: '/laserterapia'
            },
            {
              page: 'Onde d urto',
              link: '/onde-urto'
            },
            {
              page: 'Magnetoterapia',
              link: '/maggnetoterapia'
            },
            {
              page: 'Tariffario',
              link: '/tariffario'
            }
          ]
        },
        { page: 'Osteopatia',
          link: '/osteopatia'},
        { page: 'Idrokinesiterapia',
          link: '/idrokinesiterapia'},
        { page: 'Riatletizzazione',
          link: '/riatletizzazione'},
        { page: 'Neuromotoria',
          link: 'neuromotoria'},
        { page: 'Consulenze',
          link: '/consulenze',
          submenu: true
        },
        { page: 'Prodotti',
          link: 'prodotti'}
      ],
      isExpand: false 
    }
  },
  methods: {
    openSubmenu: function() {
      this.isExpand = !this.isExpand
    }
  } 
}
</script>
