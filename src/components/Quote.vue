
<template>
  <div id="quote" >

  <div class="row">
    <div class="col-sm-6">
      <div v-for="(quote,i) in quotes" :key="i" class="quote" @click="removeQuote(i)" >
      {{quote.content}}
      <p class="author"> - {{quote.author}}</p>
    </div>

    </div>
  </div>

  </div>

</template>
<script>
 export default{
    props: ['quotes'],
    methods: {
      removeQuote(i){
        this.$emit('removeQuote',i);

      }
    }

 }
</script>
<style>
.quote{
  border: 1px black solid;
  margin: 30px;
}

.author{
  color:#ccc;
}
</style>
