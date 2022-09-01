<template>
  <div id="app">
    <button type="button" class="next-button" @click="okraWidget">Next</button>
    <div class="fas fa-chevron-right next-icon" aria-hidden="true" data-v-6a7be0d0=""></div>
  </div>
</template>

<script>
import Okra from 'okra-js'

export default {
      methods: {
        okraWidget() { 
          Okra.buildWithShortUrl({
          short_url: 'cnO-f0BIz',
          onSuccess: function(data){
              //location.href = '/credit-readiness-financials?result=success';
          },
          onClose: function(){
              //location.href = '/credit-readiness-financials?result=cancel';
          }
      })
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

.next-button {
    font-family:"Bw Modelica", sans-serif;
    font-size: 14px;
    color: rgb(0, 0, 0);
    letter-spacing: 0px;
    line-height: 17px;
    position: absolute;
    left: -38px;
    top: 7px;
}

.next-icon {
  font-size: 30px;
}

</style>