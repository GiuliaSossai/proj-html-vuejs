<template>
   <div class="cover">
      <img src="../assets/img/video-1.jpg" alt="video">

      <div class="layover">
         <i class="fas fa-play"></i>
         <i class="fas fa-play"></i>
      </div>
   </div>    
</template>

<script>
export default {
   name: 'VideoSection',
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';

.contents {
   .cover {
   position: relative;
   width: 100%;
   img {
      display: block;
      }
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