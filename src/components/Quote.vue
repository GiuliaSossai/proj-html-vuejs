<template>
  <div class="extract px-4 py-5 mt-4">
      <h5>President Speech</h5>
      <i class="fas fa-quote-right"></i>
      <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. </p>
      <p class="my-2">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Itaque consequuntur, praesentium hic enim voluptates quod id magni? </p>
      <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. </p>
      <p class="my-2">T. Jhonson</p>
   </div>
</template>

<script>
export default {
   name: 'Quote'
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';
@import '../assets/style/mixins.scss';

.extract {
   width: 30%;
   min-height: 300px;
   background-color: $main-btn;
   border-radius: 5px;
   color: $light-green;
   position: relative;
   h5 {
      color: $main;
      font-size: 24px;
   }
   p:last-child {
      font-weight: 700;
      padding-top: 30px;
   }
   .fas {
      position: absolute;
      bottom: 65px;
      right: 20px;
      color: darken($main-btn , 10%);
   }
}

</style>