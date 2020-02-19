<template>
    <div class="c-methods flex flex-col justify-between">
        <div class="c-methods__item" v-for="method in methods">
          <figure>
            <img class="mx-auto" v-bind:src="method.image" alt="">
          </figure>
          <article class="c-methods__text">
            <h2 class="mb-4 uppercase">{{method.title}}</h2>
            <p>{{method.text}}</p>
          </article>
        </div>
    </div>
</template>
<script>
export default {
  data () {
    return {
      methods: [
        { 
          image: 'icona-diagnosi-precisa.png',
          title: 'valutazione specialistica e diagnosi precisa',
          text: 'Precede ogni percorso riabilitativo, per definire quadro clinico e protocollo terapeutico.'
        },
        { 
          image: 'icona-approccio-multidisciplinare.png',
          title: 'approccio multidisciplinare',
          text: 'Ci consente di accogliere il paziente, conoscere le problematiche e curarle dalle cause ai sintomi.'
        },
        { 
          image: 'icona-protocollo-riabilitativo.png',
          title: 'protocollo riabilitativo in 4 fasi',
          text: 'Per ogni percorso terapeutico, dalle prime terapie in studio, fino al ritorno al movimento o allo sport.'
        }
      ] 
    }
  }
}
</script>