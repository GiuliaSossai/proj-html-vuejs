<template>
  <main>
     <!-- 01 video -->
     <VideoSection />

     <!-- 02 numbers -->
     <ResultsSection />

     <!-- 03 services -->
     <ServicesSection />

     <!-- 04 team -->
     <section>
        <div class="container d-flex justify-content-between">
           <div class="textarea">
               <p class="subs">we like what we do</p>
               <h2><span class="special-title px-3 pb-2">Team</span> of Experts</h2>
               <p class="text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Minus fugit, quisquam voluptate optio labore exercitationem, sequi vero incidunt unde laudantium sapiente excepturi aperiam.</p>
               <div>
                  <CardsList />
               </div>     
           </div>

           <div class="extract p-3 mt-4">
              <h5>President Speech</h5>
              <i class="fas fa-quote-right"></i>
              <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. </p>
              <p class="my-2">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Itaque consequuntur, praesentium hic enim voluptates quod id magni? </p>
              <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. </p>
              <p class="my-2">T. Jhonson</p>
           </div>
        </div>
        
      </section>

     <!-- 05 news -->
     <section class="news">
         <div class="container">
            <p class="subs">our editorial content</p>
            <h2>Latest <span class="special-title px-3 pb-2">News</span></h2>
            <div class="d-flex justify-content-between align-items-center">
               <p class="text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Minus fugit, quisquam voluptate optio labore exercitationem</p>
               <button class="btn gs-solid-btn m-0">see all</button>
            </div>
            
            <EditorialContent />
         </div>
      </section>

     <!-- 06 form1 -->
     <section>Know First</section>

     <!-- 07 form2 -->
     <section>Get in Touch</section>
  </main>
</template>

<script>
// sezioni importate
import VideoSection from './VideoSection.vue';
import ResultsSection from './ResultsSection.vue';
import ServicesSection from './ServicesSection.vue';

// componenti delle sezioni 4-5
import CardsList from './CardsList.vue';
import EditorialContent from './EditorialContent.vue';

export default {
   name: 'Main',
   components: {
      VideoSection,
      ResultsSection,
      ServicesSection,

      CardsList,
      EditorialContent,

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

// 04 team
.textarea {
   width: 60%;
   .subs {
      color: $main-btn;
   }
   .text {
      color: $subtitle;
   }
}


.extract {
   width: 250px;
   min-height: 300px;
   background-color: $main-btn;
   border-radius: 5px;
   color: $subtitle;
   position: relative;
   h5 {
      color: $main;
   }
   p:last-child {
      font-weight: 700;
   }
   .fas {
      position: absolute;
      bottom: 30px;
      right: 20px;
      color: darken($main-btn , 10%);
   }
}

// 05 news
.news {
   background-color:$light-green;
   .subs {
      color: $main-btn;
   }
   .special-title {
      background-color: darken($ultra-light, 16%);
   }
   .text {
      color: $subtitle;
      width: 50%;
   }
}

</style>