<template>
  <div>
      <div class="box p-4"
         v-for="(item, index) in ServicesList"
         :key="index"
      >
         <i :class="item.icon.join(' ')"></i>
         <h5 class="my-3">{{item.title}}</h5>
         <p>{{item.sub}}</p>

         <a href=""><i class="fas fa-arrow-right"></i></a>
      </div>
   </div>
</template>

<script>
import ServicesList from "../assets/data/ServicesList.js";

export default {
   name: 'BoxesList',
   components: {
      

   },
   data(){
      return {
         ServicesList
      }
   },
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';
@import '../assets/style/mixins.scss';

.box {
   display: inline-block;
   width: 30%;
   margin: 1.5%;
   background-color: #19191E;
   color: $subtitle;
   border-radius: 5px;
   position: relative;
   i {
      font-size: 30px;
      color: $main-btn;
   }
   h5{
      color: $main;
   }

   .fa-arrow-right {
      position: absolute;
      top: 20px;
      right: 20px;
      font-size: 16px;
   }
}

.box:hover i{
   color: $main;
}
.box:hover .fa-arrow-right{
   border-radius: 50%;
   padding: 3px;
   background-color: $main-btn;
}

</style>