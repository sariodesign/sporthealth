<template>
  <div>
    <div class="c-navigation__toggle" :class="{'is-active' : isActive}" @click="openMenu()">
      <span class="font-semibold mr-2 leading-none">MENU</span>
      <div class="c-navigation__toggle-line"></div>
    </div>
    <nav class="c-navigation flex" :class="{'is-open' : isOpen }">
      <ul class="c-navigation__contact flex justify-end">
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
      <div class="c-navigation--primary">
        <Menu />
      </div>
    </nav>
  </div>  
</template>

<script>

import Menu from '~/components/Menu.vue'

export default {
  data () {
    return {
      items: [
          { 
            page: 'Chi siamo',
            link: '/chi-siamo'
          },
          { 
            page: 'Staff',
            link: '/staff'
          },
          { 
            page: 'Sedi',
            link: '/sedi',
            submenu: [
              {
                page: 'Centri Sport Health',
                link: '/centri-sport-health'
              },
              {
                page: 'Sport Health Point',
                link: '/sport-health-point'
              }
            ]
          },
          { 
            page: 'Contatti',
            link: '/contatti'
          },
      ],
      isOpen: false,
      isActive: false
    }
  },
  components: {
    Menu
  },
  methods: {
    openMenu: function() {
      this.isOpen = !this.isOpen
      this.isActive = !this.isActive
    }
  }
}
</script>