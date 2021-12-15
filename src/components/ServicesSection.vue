<template>
  <section class="services-section">
     <div class="gs-wrap">
         <p class="subs">our business area</p>
         <h2>Excellence in <span class="special-dark-title px-3 pb-2">Services</span></h2>

         <div class="d-flex justify-content-between">
            <p class="text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Minus fugit, quisquam voluptate optio labore exercitationem</p>
            
            <button class="col-1 btn gs-btn">see all</button>
         </div>
         
         <div>
            <BoxesList />
         </div>
         
     </div>
     
   </section>
</template>

<script>
import BoxesList from './BoxesList.vue';

export default {
   name: 'ServicesSection',
   components: {
      BoxesList,
   }
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';
@import '../assets/style/mixins.scss';

.services-section {
   background-color: $darkest-bg;
   color: $main;
   .subs {
      color: $main-btn;
   }
   .text {
      color: $subtitle;
   }
   
}

</style>