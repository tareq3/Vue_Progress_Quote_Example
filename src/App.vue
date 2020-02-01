<template>
  <div id="app">
      <div class="container">
        <Header :maxQuote="maxQuates" :quoteCount="quates.length"/>
        <NewQuote @submit="addQuote"/>
        <QuateGrid :quates="quates"/>

        <div class="row">
          <div class="col-sm-12 text-center">
            <div class="alert alert-info">
              click twice to delete it
            </div>
            
          </div>
          </div>
      </div>
  </div>
</template>

<script>
import QuateGrid from'./components/QuateGrid'
import NewQuote from './components/NewQuote'

import Header from './components/Header'
export default {
  name: 'app',

  data(){
    return {
        quates:['this is a quate'],
        maxQuates:5
    }
  },
  components: {
    QuateGrid,
    NewQuote,
    Header
  },
  methods:{
    hello(){
      console.log('started')
    },
    addQuote(value){
      this.quates.push(value);

    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  height: 1000px;
  padding-top: 50px;
  background-color: aliceblue;
}
</style>
