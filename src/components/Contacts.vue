<template>
  <div class="header-top">
        <div class="gs-wrap d-flex justify-content-between align-items-center py-2">
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
</template>

<script>
import ContactsHeader from "../assets/data/ContactsHeader.js";

export default {
   name: 'Contacts',
   data(){
      return {
         ContactsHeader
      }
   },
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';
@import '../assets/style/mixins.scss';

.header-top{
   background-color: darken($blue-bg, 30%);
   ul li a {
      margin: 0 10px;
      color: $subtitle;
      &:hover {
         color: $main;
         cursor: pointer;
      }      
   }
}

</style>