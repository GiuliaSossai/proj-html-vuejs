<template>
  <header>
     <div class="header-top">
        <div class="container d-flex justify-content-between align-items-center py-2">
            <div>
               <i class="fas fa-clock"></i>
               Open Hours: Mon - Sat - 9:00 - 18:00
            </div>

            <ul class="d-flex">
               <!-- ciclo for per stampare la lista -->
               <li 
                  v-for="(contact, index) in ContactsHeader"
                  :key="index"   
               >
               <a href="#">
                  <i :class="contact.icon.join(' ')"></i>
                  {{contact.text}} 
               </a>   
               </li>
            </ul>
         </div>
      </div>

      
      
      <div class="jumbotron">
         <div class="container">
            <div class="d-flex justify-content-between align-items-center pt-3 jumbo-top">
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
                     <a href="#"> {{item.text}} </a>
                     <i :class="item.icon.join(' ')"></i>
                  </li>
               </ul>   
            </div>

            <div class="jumbo-bottom">
               <h1 class="text-center">Financial Risk</h1>
               <p class="text-center">The right outcomes depends on continuos rigor in governance, models, and processes across the finance function.</p>
               <div class="text-center pt-4">
                  <button class="btn gs-solid-btn">get in touch</button>
                  <button class="btn gs-btn">read more</button>
               </div>   
            </div>
            
         </div>
         
      </div>
  </header>
</template>

<script>
import ContactsHeader from "../assets/data/ContactsHeader.js";
import MenuHeader from "../assets/data/MenuHeader.js";


export default {
   name: 'Header',
   components: {
      
   },
   data(){
      return {
         counter: 6,
         ContactsHeader,
         MenuHeader
      }
   },
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';
@import '../assets/style/mixins.scss';

header {
   color: $subtitle;
   .header-top{
      background-color: darken($blue-bg, 30%);
      ul li a {
         margin: 0 10px;
         color: $subtitle;
         &:hover {
            color: $main;
         }
         
      }
   }

   .jumbotron {
      height: 600px;
      background-image: url('../assets/img/bg-2.jpg');
      @include bg-position;
      .jumbo-top {
         margin-bottom: 10%;
         .logo {
         width: 120px;
         }

         .menu {
            text-transform: uppercase;
            a {
               padding: 0 20px;
               color: lighten($subtitle, 20%);
               &:hover {
               color: $subtitle;
               }
            }
            .active {
               background-color: $main-btn;
            }
         }
      }

      .jumbo-bottom{
         @include gs-wrap;
         h1 {
            font-size: 60px;
            margin-bottom: 20px;
            color: $main;
         }
         p{
            font-size: 20px;
         }
         .gs-solid-btn{
            color: $main;
            background-color: $main-btn;
            margin-right: 10px;
         }
         .gs-btn {
            color: $main;
            border: 1px solid $main-btn;
            &:hover {
               background-color: $main-btn;
            }
         }
      }  
   }
}

</style>