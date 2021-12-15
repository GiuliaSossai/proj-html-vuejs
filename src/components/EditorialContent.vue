<template>
  <div class="d-flex align-items-center justify-content-between mt-4">
     <div class="ed-box text-center cover mt-3"
      v-for="(item, index) in Editorials"
      :key="index"
     >
         <img :src="require(`../assets/img/${item.image}`)" :alt="item.title">

         <a href="#">
            <div class="layover p-4">
               <div class="d-flex justify-content-between">
                  <p><i class="far fa-user me-2"></i>{{item.author}}</p>
                  <p><i class="far fa-clock me-2"></i>{{item.date}}</p>
               </div>
               <h5>{{item.title}}</h5>
               <p>{{item.text}}</p>
            </div>
         </a>
     </div>
  </div>
</template>

<script>
import Editorials from '../assets/data/Editorials';

export default {
   name: 'EditorialContent',
   components: {
      
   },
   data(){
      return {
         Editorials
      }
   }
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';
@import '../assets/style/mixins.scss';

.ed-box {
   width: 30%;
   border-radius: 8px;
   overflow: hidden;
   min-height: 100px;
   position: relative;
   img {
      display: block;
   }
   &:hover img {
      filter:blur(5px);
   }

   .layover {
      position: absolute;
      top: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.5);
      color: $main;
      p {
         display: none;
      }
      h5 {
         margin-top: 50%;
      }
      &:hover p{
         display: block;
      }
      &:hover h5{
         margin-top: 30%;
      }
   }


}
</style>