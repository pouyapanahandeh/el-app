<template>
  <q-page>
    <SearchComp />
    <ResultCards />
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'
import SearchComp from 'src/components/SearchComp.vue';
import ResultCards from 'src/components/ResultCards.vue';
export default defineComponent({
  components:{
    SearchComp,
    ResultCards
},
  name: 'IndexPage'
})
</script>
<style>
body{
  background-color: #0F172A;
}
</style>
