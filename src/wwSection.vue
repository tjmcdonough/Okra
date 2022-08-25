<template>
  <div id="app">
    <button v-on:click="okrawidget">Open Widget</button>
  </div>
</template>

<script>
import Okra from 'okra-js'

export default {
      methods: {
        okrawidget: Okra.buildWithShortUrl({
        short_url: 'izX93-Rx5',
        onSuccess: function(data){
            //location.href = '/credit-readiness-financials?result=success';
        },
        onClose: function(){
            //location.href = '/credit-readiness-financials?result=cancel';
        }
    })
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

</style>