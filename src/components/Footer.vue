<template>
  <footer>
     <div class="footer-top gs-lgt">
        <div class="gs-wrap row">
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

            <FooterMenu :footerList = "aboutList" class="col footer-menu py-4"/>
            <FooterMenu :footerList = "servicesList" class="col footer-menu py-4"/>
            <FooterMenu :footerList = "supportList" class="col footer-menu py-4"/>
        </div>
     </div>

     <!-- footer-bottom -->
     <div class="footer-bottom gs-lgt">
        <div class="gs-wrap d-flex justify-content-between align-items-center py-4">
            <p>Enjoy the low price. We are tracking any intention of piracy</p> 
            <p>&copy; 2020 NEXGEN is proudly powered by <span>Codings</span>.</p>
         </div>
     </div>
  </footer>
</template>

<script>
import FooterMenu from './FooterMenu.vue';

import ContactsSmall from "../assets/data/ContactsSmall.js";

export default {
   name: 'Footer',
   components: {
      FooterMenu,   
   },

   data(){
      return {
         ContactsSmall,

         aboutList: {
            id: "1",
            name: 'About',
            elements: ['The Company', 'Institutional', 'Social & Events', 'Innovation', 'Environment', 'Technology']
         },

         servicesList: {
            id: "2",
            name: 'Services',
            elements: ['Audit & Assurance', 'Financial Advisory', 'Analytics M&A', 'Middle Marketing', 'Legal Consulting', 'Regulatory Risk']
         },

         supportList: {
            id: "3",
            name: 'Support',
            elements: ['Responsability', 'Terms of Use', 'About Cookies', 'Privacy Policy', 'Accessibility', 'Information']
         }  
      }
   }
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';
@import '../assets/style/mixins.scss';

.footer-top {
   background-image: url('../assets/img/bg-7.jpg');
   min-height: 300px;
   @include bg-position;
   padding: 80px 0;
   a {   
      
      &:hover {
         color: $main;
      }
   }

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
         min-height: 100px;
         background-color: rgba(182, 181, 181, 0.1);
         border-radius: 5px;
         h5 {
            color: $main;
         }
      }
   }
}

.footer-bottom{
   background-color: $dark-bg;
   p {
      margin: 0;
      span {
         color: $main-btn;
      }
   }
}

</style>