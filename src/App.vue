<template>
  <div id="app">
    <div class="row">
      <div class="col-10 offset-1">
        <div class=" progressbar">
            <div class="progress">
            </div>
        </div>

      </div>
    </div>

    <app-quotes></app-quotes>
  </div>
</template>

<script>
import Quotes from './components/Quotes.vue'

export default {
  name: 'App',
  components: {
    appQuotes:Quotes
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

.progressbar{

  border: 1px lightgrey solid;
  height: 30px;
  border-radius: 10px;
  z-index: -2;

}
.progress{position: absolute;
  height: 29px;
  border-radius: 10px;

  }
</style>
