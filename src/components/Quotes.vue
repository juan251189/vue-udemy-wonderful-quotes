<template>
<div id="quotes">



      <app-quote :quotes="quotes">

      </app-quote>



</div>
</template>
<script>
import Quote from './Quote.vue'
export default {

  data: () => ({
    quotes: [{
        content: "The greatest glory in living lies not in never falling, but in rising every time we fall.",
        author: 'Nelson Mandela'
      },
      {
        content: "The way to get started is to quit talking and begin doing.",
        author: 'Walt Disney'
      },
      {
        content:"our time is limited, so don't waste it living someone else's life. Don't be trapped by dogma – which is living with the results of other people's thinking",
        author:'Steve Jobs'
      },
      {
        content:"If life were predictable it would cease to be life, and be without flavor.",
        author:'Eleanor Roosevelt'
      }
    ]
  }),
  components: {
    appQuote:Quote
  }
}
</script>
<style  scoped>
</style>
