<template>
  <div class="menu-content">
         <div class="gs-wrap">
            <div class="d-flex justify-content-between align-items-center pt-3 menu-top">
               <div class="logo">
                  <a href="#"><img src="../assets/img/nexgen-logo.svg" alt="nexgen-logo"></a>
               </div>
               
               <ul class="menu d-flex">
                  <!-- ciclo for per stampare la lista -->
                  <!-- se la voce del menu è attiva, assume la classe active -->
                  <li
                     v-for="(item, index) in MenuHeader"
                     :key="index"
                     :class="{active : (index === counter)}"
                     @click="counter = index"
                  >
                     <a :href="item.href"> {{item.text}} 
                     <i :class="item.icon.join(' ')"></i></a>
                  </li>
               </ul>   
            </div>

            <div class="menu-bottom">
               <h1 class="text-center">Financial Risk</h1>
               <p class="text-center gs-lgt">The right outcomes depends on continuos rigor in governance, models, and processes across the finance function.</p>
               <div class="text-center pt-4">
                  <button class="btn gs-solid-btn me-3">get in touch</button>
                  <button class="btn gs-btn">read more</button>
               </div>   
            </div>
            
         </div>  
      </div>
</template>

<script>
import MenuHeader from "../assets/data/MenuHeader.js";

export default {
   name: 'Menu',
   data(){
      return {
         counter: 6,
         MenuHeader
      }
   }

}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';
@import '../assets/style/mixins.scss';

.menu-content {
   height: 800px;
   background-image: url('../assets/img/bg-2.jpg');
   @include bg-position;
   .menu-top {
      margin-bottom: 10%;
      .logo {
         width: 120px;
      }

      .menu {
         color: $main;
         text-transform: uppercase;
         li {
            margin: 0 10px;
            padding: 10px 15px;
         }
         a {
            color: lighten($subtitle, 20%);
            font-size: 20px;
            &:hover {
               color: $subtitle;
            }
         }
         .active {
            background-color: $main-btn;
            border-radius: 4px;
         }
         
      }
   }

   .menu-bottom{
      @include gs-wrap;
      h1 {
         margin-top: 35%;
         margin-bottom: 20px;
         color: $main;
      }
      p{
         font-size: 24px;
      }
   }  
}
</style>