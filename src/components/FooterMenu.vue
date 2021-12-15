<template>
   <div>
      <div v-for="(item, index) in footerList" :key="index">
         <h5></h5>
      </div>
         
         <ul>
            <li
               v-for="(item, index) in footerList.elements"
               :key="index"
            >
               <i class="fas fa-chevron-right"></i>
               <a href=""> {{item}} </a>
            </li>  
         </ul>
      
   </div>
   
</template>

<script>
export default {
   name: 'FooterMenu',
   props: {
      footerList: Object
   }
}
</script>

<style>

</style>