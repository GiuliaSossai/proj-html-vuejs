<template>
  <div class="col footer-menu py-4 px-3">
      <h5>About</h5>
      <ul>
         <li
            v-for="(item, index) in aboutList"
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
   name: 'AboutFooter',
   props: {
      aboutList: Array
   }
}
</script>

<style>

</style>