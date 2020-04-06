<template>
  <section class="c-categories">
    <h1 class="o-heading text-center uppercase py-4">Sport Health: fisioterapia e riatletizzazione a Roma e fuori città</h1>
    <div class="c-categories__group">
      <div v-for="category in categories" :key="category.id" class="c-categories__item">
        <div class="c-categories__content">
          <div class="c-categories__text">
            <h2 class="o-heading font-bold leading-none mb-1">{{category.name}}</h2>
            <p class="o-text leading-tight mb-1">{{category.text}}</p>
          </div>
          <nuxt-link class="c-navigation__link" :to=category.link>
            <button class="o-button o-button--secondary" data-label="Scopri di più"></button>
          </nuxt-link>
        </div>
      </div>
    </div> 
  </section>
</template>
<script>
  export default {
      data () {
        return {
          categories: [
          { name: 'Fisioterapia',
            text: 'Le terapie manuali rappresentano il primo approccio riabilitativo',
            link: '/fisioterapia'},
          { name: 'Idrokinesiterapia',
            text: 'L’utilizzo dell’acqua come migliore alleata a scopo terapeutico',
            link: '/idrokinesiterapia'},
          { name: 'Riatletizzazione',
            text: 'Un trainer personale per migliorare l’efficienza fisica e le performance di atleti',
            link: '/riatletizzazione'},
          { name: 'Neuromotoria',
            text: 'L’apprendimento o il riapprendimento del movimento',
            link: '/neuromotoria'},
          { name: 'FisioEstetica',
            text: 'Le terapie manuali rappresentano il primo approccio riabilitativo',
            link: '/fisioterapia'}
        ]
      }
    }
  }
</script>