<template>
  <section class="results-bg">
        <div class="contents text-center">
            <p class="subs">what are we doing</p>
            <h2><span class="special-dark-title px-3 pb-2">Results</span> in Numbers</h2>
         </div>

         <div class="gs-wrap row text-center">
            <div class="col"
               v-for="(item, index) in Results"
               :key="index"
            >
               <h4>{{item.quantity}}</h4>
               <h5>{{item.text}}</h5>
            </div>
         </div>
   </section>
</template>

<script>
import Results from "../assets/data/Results.js";

export default {
   name: 'ResultsSection',
   data(){
      return {
         Results
      }
   },
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';
@import '../assets/style/mixins.scss';

.results-bg {
   background-image: url('../assets/img/bg-1.jpg');
   @include bg-position;
   h2, h5{
      color: $main;
   }
   .row {
      margin: 30px auto;
      h4 {
         color: $main-btn;
         font-size: 32px;
      }
      h5 {
         font-size: 25px;
      } 
   }  
}
</style>