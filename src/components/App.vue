<template>
  <div id="app">

<div>
  <h1>{{state.counterValue}}</h1>
  <button v-on:click="increment">+</button>
</div>

  </div>
</template>

<script>
const store = {
  debug: true,
  state: {
    counterValue: 0
  },
  increment() {
    console.log('updating counterValue...')
    store.state.counterValue++
    console.log(store.state.counterValue)
  }
}


module.exports = {
  data() {
      return {
        state: store.state
      }
    },
    methods: {
      increment: function() {
        store.increment()
      }
    }

}
</script>

<style>
  body {
    text-align: center;
    font-family: Helvetica, sans-serif;
  }
</style>
