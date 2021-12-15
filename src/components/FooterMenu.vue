<template>
   <div>
      <div v-for="item in footerList" :key="item.id">
         <h5 class="px-4">{{item}}</h5>
      </div>
         
      <ul>
         <li
            class="px-4 py-1"
            v-for="(item, index) in footerList.elements"
            :key="index"
         >
            <i class="fas fa-chevron-right"></i>
            <a href="#" class="gs-lgt"> {{item}} </a>
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