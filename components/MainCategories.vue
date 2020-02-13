<template>
  <section class="c-categories">
    <h1>SPORT HEALTH: FISIOTERAPIA E RIATLETIZZAZIONE A ROMA E FUORI CITTÀ</h1>
    <div v-for="category in categories" :key="category.id" class="c-categories__item">
      <h2>{{category.name}}</h2>
      <p>{{category.text}}</p>
    </div> 
  </section>
</template>
<script>
  export default {
      data () {
        return {
          categories: [
          { name: 'Fisioterapia',
            background: '',
            text: 'Le terapie manuali rappresentano il primo approccio riabilitativo',
            link: ''},
          { name: 'Idrokinesiterapia',
            background: '',
            text: 'L’utilizzo dell’acqua come migliore alleata a scopo terapeutico',
            link: ''},
          { name: 'Riatletizzazione',
            background: '',
            text: 'Un trainer personale per migliorare l’efficienza fisica e le performance di atleti',
            link: ''},
          { name: 'Neuromotoria',
            background: '',
            text: 'L’apprendimento o il riapprendimento del movimento',
            link: ''},
          { name: 'FisioEstetica',
            background: '',
            text: '',
            link: ''}
        ]
      }
    }
  }
</script>