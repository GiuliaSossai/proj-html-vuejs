<template>
   <div class="row">
      <div class="col contacts-menu">
         <div class="logo mb-3">
            <img src="../assets/img/nexgen-logo.svg" alt="nexgen-logo">
         </div>
         <p>A Functional HTML Template for Corporate & Business.</p>

         <ul class="my-4">
            <li
               class="my-2"
               v-for="(contact, index) in ContactsSmall"
               :key="index"   
            >
               <a href="#" class="gs-lgt">
                  <i :class="contact.icon.join(' ')"></i>
                  {{contact.text}} 
               </a>   
            </li>
         </ul>

         <button class="btn gs-btn mt-2">get in touch</button>
      </div>


      <div v-for="item in footerList" :key="item.id" class="col footer-menu">
         <h5 class="px-4">{{item.name}}</h5>
      
         <ul>
            <li
               class="px-4 py-1"
               v-for="(li, index) in item.elements"
               :key="index"
            >
               <i class="fas fa-chevron-right"></i>
               <a href="#" class="gs-lgt"> {{li}} </a>
            </li>  
         </ul>
      </div>  
   </div>
   
</template>

<script>
import ContactsSmall from "../assets/data/ContactsSmall.js";

export default {
   name: 'FooterMenu',
   props: {
      footerList: Array
   },
   data(){
      return{
        ContactsSmall 
      }
      
   }
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';
@import '../assets/style/mixins.scss';

.row {
   margin: 0 auto;
   .contacts-menu{   
      .logo {
         cursor: pointer;
         width: 120px;
      }
      .fas {
         font-size: 14px;
         color: lighten($subtitle, 30%);
      }
   }
   .footer-menu {
      margin: 0 15px;
      padding: 35px 20px;
      min-height: 100px;
      background-color: rgba(182, 181, 181, 0.1);
      border-radius: 5px;
      h5 {
         color: $main;
         font-size: 22px;
      }
      a {
         font-size: 18px;
      }
   }        
}

</style>