<template>
  <nav class="c-navigation flex flex-col">
    <ul class="c-navigation__contact flex justify-end">
      <li class="c-navigation__item">
        <nuxt-link class="c-navigation__link" to="/chi-siamo"
          >Chi siamo</nuxt-link
        >
      </li>
      <li class="c-navigation__item">
        <nuxt-link class="c-navigation__link" to="/staff">Staff</nuxt-link>
      </li>
      <li class="c-navigation__item">
        <nuxt-link class="c-navigation__link" to="/contatti"
          >Contatti</nuxt-link
        >
      </li>
      <li class="c-navigation__item">
        <nuxt-link class="c-navigation__link" to="/sedi">Sedi</nuxt-link>
      </li>
    </ul>
    <div class="c-navigation--primary">
      <Menu />
    </div>
  </nav>
</template>
<script>

import Menu from '~/components/Menu.vue'

export default {
  components: {
    Menu
  }
}
</script>