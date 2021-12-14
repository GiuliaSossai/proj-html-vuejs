<template>
  <section class="services-section">
     <div class="container">
         <p class="subs">our business area</p>
         <h2>Excellence in <span class="special-dark-title px-3 pb-2">Services</span></h2>

         <div class="row">
            <div class="col-11">
               <p class="text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Minus fugit, quisquam voluptate optio labore exercitationem, sequi vero incidunt unde laudantium sapiente excepturi aperiam.</p>
            </div>
            <button class="col-1 btn gs-btn">see all</button>
         </div>

         <div class="row">
            <div class="col-4 box">
               ciao
            </div>
         </div>
     </div>
     
   </section>
</template>

<script>
export default {
   name: 'ServicesSection'
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
   .box {
      min-height: 100px;
      background-color: #19191E;
      color: $subtitle;
      border-radius: 5px;
   }
}

</style>