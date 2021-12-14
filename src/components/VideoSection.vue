<template>
  <section class="container">
      <div class="contents text-center">
         <p class="subs">introduction video</p>
         <h2>Advisory <span class="special-title px-3 pb-2">Performance</span></h2>
         <p class="text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Minus fugit, quisquam voluptate optio labore exercitationem, sequi vero incidunt unde laudantium sapiente excepturi aperiam.</p>

         <div class="cover">
            <img src="../assets/img/video-1.jpg" alt="video">

            <div class="layover">
               <i class="fas fa-play"></i>
               <i class="fas fa-play"></i>
            </div>
         </div>

      </div>   
   </section>
</template>

<script>
export default {
   name: 'VideoSection',
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';
@import '../assets/style/mixins.scss';

.contents {
   @include gs-wrap;
   .subs {
      color: $main-btn;
   }
   
   .text{
      color: $subtitle;
   }

   .cover {
   position: relative;
   width: 100%;
   }

   .cover img {
   width: 100%;
   display: block;
   }

   .layover {
   position: absolute;
   top: 0;
   display: none;
   width: 100%;
   height: 100%;
   background-color: rgba(8, 109, 84, 0.2);
   text-align: center;
   }

   .fa-play {
   color: $main;
   font-size: 50px;
   position: absolute;
   top: 50%;
   left: 50%;
   transform: translate(-50%, -50%);
   &:hover {
      cursor: pointer;
      }
   }
   .fa-play:last-child{
      color: $main-btn;
      opacity: 30%;
      font-size: 50px;
      position: absolute;
      top: 48%;
      left: 50%;
      transform: translate(-50%, -50%);
   }

   .cover:hover .layover {
   display: block;
   }
}

</style>