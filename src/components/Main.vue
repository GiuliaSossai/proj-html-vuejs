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
        <div class="gs-wrap d-flex justify-content-between">
           <div class="textarea">
               <p class="subs">we like what we do</p>
               <h2><span class="special-title px-3 pb-2">Team</span> of Experts</h2>
               <p class="text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Minus fugit, quisquam voluptate optio labore exercitationem, sequi vero incidunt unde laudantium sapiente excepturi aperiam.</p>
               <div>
                  <CardsList />
               </div>     
           </div>

           <div class="extract px-4 py-5 mt-4">
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
         <div class="gs-wrap">
            <p class="subs">our editorial content</p>
            <h2>Latest <span class="special-title px-3 pb-2">News</span></h2>
            <div class="d-flex justify-content-between align-items-center">
               <p class="text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Minus fugit, quisquam voluptate optio labore exercitationem</p>
               <button class="btn gs-solid-btn m-0">see all</button>
            </div>
            
            <EditorialContent />
         </div>
      </section>

     <!-- 06 newsletter -->
     <section class="know-form">
        <div class="gs-wrap">
           <NewsLetter />
        </div>  
     </section>

     <!-- 07 form2 -->
     <section>
        <div class="gs-wrap d-flex justify-content-between align-items-center">
           <Form />

           <div class="contacts">
              <h4>Example Inc.</h4>
              <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
              <p>Culpa adipisci esse voluptatem quo corporis, vel suscipit dolor distinctio! Quibusdam, accusamus dolores ratione </p>
              <ul>
                  <li 
                     v-for="(contact, index) in ContactsSmall"
                     :key="index"   
                  >
                     <a href="#">
                        <i :class="contact.icon.join(' ')" class="p-2"></i>
                        {{contact.text}} 
                     </a>   
                  </li>
               </ul>
               <button class="btn gs-btn p-2 mt-3">view map</button>
           </div>
        </div>
     </section>
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

//componenti form sezioni 06-07
import NewsLetter from './NewsLetter.vue';
import Form from './Form.vue';

//per sezione form2 e footer prima colonna
import ContactsSmall from "../assets/data/ContactsSmall.js";

export default {
   name: 'Main',
   components: {
      VideoSection,
      ResultsSection,
      ServicesSection,

      CardsList,
      EditorialContent,

      NewsLetter,
      Form,
      

   },
   data(){
      return {
         ContactsSmall,
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

// 05 news
.news {
   background-color: $light-green;
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

// 06 - newsletter
.know-form {
   background-color: $darkest-bg;
}

// 07 - form
.contacts {
   width: 30%;
   p {
      color: $subtitle;
   }
   a:hover {
      color: $darkest-bg;
   }
   a i{
     border-radius: 50%;
     background-color: $light-green;
     margin: 8px;
   }
   a, .gs-btn {
      color: $main-btn;
   }
}

</style>