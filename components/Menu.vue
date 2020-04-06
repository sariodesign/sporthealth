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
            <template v-if="item.submenu">
              <div class="c-navigation__toggle-submenu" v-on:click="openSubmenu($event.target)"></div>
              <ul class="c-navigation__submenu">
                <li class="c-navigation__subitem" v-for="subitem in item.submenu" :key="subitem.id">
                  <nuxt-link class="c-navigation__link" :to=subitem.link>
                    {{subitem.page}}
                  </nuxt-link>
                </li>
              </ul>
            </template>
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
            link: '/medici-e-centri-collegati',
            submenu: [
              {
                page: 'Medici e Centri Collegati',
                link: '/medici-e-centri-collegati'
              },
              {
                page: 'Nutrizione',
                link: '/nutrizione'
              },
              {
                page: 'Personal trainer',
                link: '/personal-trainer'
              }
            ]
          },
          { page: 'Prodotti',
            link: 'prodotti'}
        ]
      }
    },
    methods: {
      openSubmenu: function(el) {
        let submenu = el.nextElementSibling;
        el.classList.toggle('is-active');
        submenu.classList.toggle('is-expanded');
      }
    } 
  }
</script>
