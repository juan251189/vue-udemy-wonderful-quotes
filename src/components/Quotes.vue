<template>
<div id="quotes">



      <app-quote :quotes="quotes" @removeQuote="deleteQuote(i)">

      </app-quote>



</div>
</template>
<script>
import Quote from './Quote.vue'
export default {

  data: () => ({

  }),
  props: ['quotes','progress'],
  components: {
    appQuote:Quote
  },
  methods: {
    deleteQuote(i){
      this.quotes.splice(i,1);
      this.progress-=1;
    }
  }

}
</script>
<style  scoped>
</style>
