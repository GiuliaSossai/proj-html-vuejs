<template>
  <div class="col footer-menu py-4 px-3">
      <h5>Services</h5>
      <ul>
         <li
            v-for="(item, index) in servicesList"
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
   name: 'ServicesFooter',
   props: {
      servicesList: Array
   }
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';
@import '../assets/style/mixins.scss';

</style>