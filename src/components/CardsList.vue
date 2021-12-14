<template>
   <div class="">
      <div 
         class="member-box"
         v-for="(item, index) in TeamList"
         :key="index"
      >
         <!-- <img src="" alt=""> -->
         <div class="member-image me-3 mb-4">
            <img src="../assets/img/team-1.jpg"/> 
            <!-- <img :src=" '..assets/img/ + ${{item.image}}' " :alt="item.name"> -->
         </div>

         <div class="member-text">
            <h5>{{item.name}}</h5>
            <p class="text-uppercase">{{item.role}}</p>
            <i :class="item.social[0]" class="p-2"></i>
            <i :class="item.social[1]" class="mx-2 p-2"></i>
            <i :class="item.social[2]" class="p-2"></i>
            <!-- <i :class="item.social.join(' ')"></i> -->
         </div>
         
      </div>
   </div>
</template>

<script>
import TeamList from "../assets/data/TeamList.js";

export default {
   name: 'CardsList',
   components: {
      

   },
   data(){
      return {
         TeamList
      }
   },
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';
@import '../assets/style/mixins.scss';

.member-box {
   display: inline-block;
   width: 50%;
   .member-image {
      float: left;
      width: 90px;
      background-color: pink;
      border-radius: 3px;
      overflow: hidden;
   }
   .member-text {
      p {
         color: $subtitle;
         font-size: 14px;
      }
      i {
         color: $main-btn;
         border-radius: 50%;
         background-color: $ultra-light;
      }
   }
}
</style>