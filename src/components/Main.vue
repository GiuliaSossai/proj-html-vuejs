<template>
  <main>
     <!-- 01 video -->
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

     <!-- 02 numbers -->
     <section class="results-bg">
        Results in Numbers
        <div class="contents text-center">
            <p class="subs">what are we doing</p>
            <h2><span class="special-dark-title px-3 pb-2">Results</span> in Numbers</h2>
         </div>

         <div class="container row text-center">
            <div class="col">
               <h4>128</h4>
               <h5>Certifications</h5>
            </div>
            <div class="col">
               <h4>230</h4>
               <h5>Employees</h5>
            </div>
            <div class="col">
               <h4>517</h4>
               <h5>Customers</h5>
            </div>
            <div class="col">
               <h4>94</h4>
               <h5>Countries Served</h5>
            </div>
         </div>
      </section>

     <!-- 03 services -->
     <section>Excellence in Services</section>

     <!-- 04 team -->
     <section>Team of Expert</section>

     <!-- 05 news -->
     <section>Latest News</section>

     <!-- 06 form1 -->
     <section>Know First</section>

     <!-- 07 form2 -->
     <section>Get in Touch</section>
  </main>
</template>

<script>
export default {
   name: 'Main',
   components: {
      
   },
   data(){
      return {
         
      }
   },
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

// seconda sezione
.results-bg {
   background-image: url('../assets/img/bg-1.jpg');
   @include bg-position;
   h2, h5{
      color: $main;
   }
   .row {
      margin: 30px auto;
      h4 {
         color: $main-btn;
         font-size: 32px;
      }
      h5 {
         font-size: 25px;
      } 
   }
   
}

</style>