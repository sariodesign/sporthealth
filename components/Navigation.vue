<template>
  <div>
    <div class="c-navigation__toggle" :class="{'is-active' : isActive}" @click="openMenu()">
      <div class="c-navigation__toggle-line"></div>
    </div>
    <nav class="c-navigation flex" :class="{'is-open' : isOpen }">
      <ul class="c-navigation__contact flex justify-end">
        <li class="c-navigation__item">
          <nuxt-link class="c-navigation__link" to="/chi-siamo">Chi siamo</nuxt-link>
        </li>
        <li class="c-navigation__item">
          <nuxt-link class="c-navigation__link" to="/staff">Staff</nuxt-link>
        </li>
        <li class="c-navigation__item">
          <nuxt-link class="c-navigation__link" to="/contatti">Contatti</nuxt-link>
        </li>
        <li class="c-navigation__item">
          <nuxt-link class="c-navigation__link" to="/sedi">Sedi</nuxt-link>
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