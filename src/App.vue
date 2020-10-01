<template>
<div id="app">
  <div class="container">
  <div class="row">
    <div class="col-10 offset-1">
      <div class=" progressbar">
        <div class="progress" :style="'width:'+progress+'0%'">
              {{progress}}/{{maxQuotes}}
        </div>
      </div>

    </div>
  </div>

    <div>
        <input type="text" class="input-quotes"
        v-model="content">
        <br>
        <button class="btn btn-primary"
        @click="addQuote"
        >Add</button>
    </div>


  <app-quotes :quotes="quotes" :progress="progress"></app-quotes>
  </div>
</div>
</template>

<script>
import Quotes from './components/Quotes.vue'

export default {
  name: 'App',
  data() {
    return {
      maxQuotes:10,
      progress: 0,
      content:'',
      quotes: [{
          content: "The greatest glory in living lies not in never falling, but in rising every time we fall.",
          author: 'Nelson Mandela'
        }

      ]
    }
  },
  components: {
    appQuotes: Quotes
  },
  methods:{
    addQuote(){

      if(this.progress<10){
        this.quotes.push({content:this.content,author:'Unknown'});
        this.progress++;
    }
      else{alert('you have reached the maxmium quotes allow')}
  }

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.progressbar {

  border: 1px lightgrey solid;
  height: 30px;
  border-radius: 10px;
  z-index: -1;
  position: relative;


}

.progress {
  position: absolute;
  height: 29px;
  border-radius: 10px;
  background-color: #4a87ba;
  justify-content: center;
  align-items: center;
  color:white;
}

.input-quotes{
  height: 100px;
  border:1px solid #ccc;
  margin: 30px auto;
  min-width: 330px;
  padding: 10px;
  justify-content: center;

}
</style>
