<template>
  <div class="container">
    <offer-block></offer-block>
  </div>
</template>

<script>

import OfferBlock from '@/components/OfferBlock/offer-block.vue';
export default {
  components:{
    OfferBlock
  }

}
</script>

<style>
* {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 0px;
  padding: 0px;
}
.container{
  display: flex;
  flex-direction: column;
}
</style>
