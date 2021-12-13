<template>
  <header>
     <div class="header-top">
        <div class="container d-flex justify-content-between align-items-center py-2">
            <div>
               <i class="fas fa-clock"></i>
               Open Hours: Mon - Sat - 9:00 - 18:00
            </div>

            <ul class="d-flex">
               <!-- <li><a href="#"> <i class="fas fa-phone"></i> +1 (035) 1234-5678 </a></li>
               <li><a href="#"> <i class="fas fa-envelope"></i> hello@example.com </a></li>
               <li><a href="#"> <i class="fab fa-facebook-f"></i> </a></li>
               <li><a href="#"> <i class="fab fa-twitter"></i> </a></li>
               <li><a href="#"> <i class="fab fa-linkedin-in"></i> </a></li>   -->
               <li 
                  v-for="(contact, index) in ContactsHeader"
                  :key="index"
               >
               <a href="#"> {{contact.text}} </a>   
               </li>
            </ul>
         </div>
      </div>
      
      <div class="jumbotron">
         <div class="container">
            <div class="d-flex justify-content-between align-items-center pt-3">
               <div class="logo">
                  <a href="#"><img src="../assets/img/nexgen-logo.svg" alt="nexgen-logo"></a>
               </div>
               
               <ul class="menu d-flex">
                  <!-- <li><a href="#"> home </a></li>
                  <li><a href="#"> about </a></li>
                  <li><a href="#"> services </a></li>
                  <li><a href="#"> team </a></li>
                  <li><a href="#"> blog </a></li>
                  <li><a href="#"> <i class="far fa-user"></i>  </a></li>   
                  <li><a href="#" class="fake-btn"> get in touch  </a></li>    -->
                  <li
                  v-for="(item, index) in MenuHeader"
                  :key="index">
                     <a href="#"> {{item.text}} </a>
                  </li>
               </ul>
               
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
            color: #fff;
         }
         
      }
   }

   .jumbotron {
      height: 600px;
      background-image: url('../assets/img/bg-2.jpg');
      @include bg-position;
      .logo {
         width: 120px;
      }

      .menu {
         text-transform: uppercase;
         a {
            margin: 0 20px;
            color: lighten($subtitle, 20%);
            &:hover {
            color: $subtitle;
            }
         }
         .fake-btn {
            padding: 5px 20px;
            background-color: $main-btn;
         }
      }
   }
}

</style>