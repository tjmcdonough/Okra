<template>
  <div id="app">
    <button v-on:click="okrawidget">Open Widget</button>
  </div>
</template>

<script>
import Okra from 'okra-js'

export default {
      methods: {
        okrawidget: Okra.buildWithOptions({
        name: 'Bnkability',
        env: 'production-sandbox',
        app_id: 'https://app.okra.ng/Ht63Wbkps',// app_id from your app builder
        key: '2eaebfb3-a036-504c-8a2a-3cc192109ff1', // Your key from the Okra dashboard
        token: '60a24b9d80c1940297279802', // Your token from the okra dashboard
        products: ['auth','identity','balance','transactions', 'income'], //in lowercase
        onSuccess: function(data){
            // POST to API
        },
        onClose: function(){
            // Go back 
            //location.href = 'credit-readiness-financials?result=cancel';
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

body#okra-widget-body {
    background-color: rgba(0,0,0,0.5) !important;
}

</style>