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
     <section class="know-form">
        <div class="content d-flex justify-content-between align-items-center">
           <div class="textarea">
               <p class="subs">newsletter</p>
               <h2><span class="special-dark-title px-3 pb-2">Know</span> first</h2>
               <p>Follow closely and receive content about our company and the news of the current market</p>
           </div>
           
           <div class="form">
              <input type="text" class="form-control d-block" placeholder="Name" aria-label="Name" aria-describedby="basic-addon1">
              <input type="text" class="form-control d-block my-3" placeholder="Email" aria-label="Email" aria-describedby="basic-addon1">
              <button class="btn gs-solid-btn">subscribe</button>
           </div>
        </div>
     </section>

     <!-- 07 form2 -->
     <section>
        <div class="container d-flex justify-content-between align-items-center">
           <div class="form pe-5">
               <p class="subs">send a message</p>
               <h2>Get in <span class="special-title px-3 pb-2">Touch</span></h2>
               <p>We will respond to your message as soon as possible</p>

                  <div class="d-flex justify-content-between">
                     <!-- input con favicon -->
                     <div class="input-inner">
                        <i class="fas fa-print"></i>
                        <input type="text" class="form-control gs-form mb-3 gs-input" placeholder="Name" aria-label="Username" aria-describedby="basic-addon1">
                     </div>
                     
                     <input type="text" class="form-control gs-form mb-3" placeholder="Email" aria-label="Email" aria-describedby="basic-addon1">
                  </div>
                  <div class="d-flex justify-content-between">
                     <input type="text" class="form-control gs-form mb-3" placeholder="Phone" aria-label="Phone" aria-describedby="basic-addon1">

                     <select name="" id="selectioninfo" class="gs-form mb-3 px-2">
                        <option value="">More Info</option>
                        <option value="">Job Oportunities</option>
                        <option value="">Consultant Request</option>
                     </select>

                  </div>
                  <textarea class="form-control mb-3"  placeholder="Message" aria-label="Message"></textarea>

                  <button class="btn gs-solid-btn">send</button>
               
           </div>

           <div class="contacts">
              <h4>Example Inc.</h4>
              <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
              <p>Culpa adipisci esse voluptatem quo corporis, vel suscipit dolor distinctio! Quibusdam, accusamus dolores ratione </p>
              <ul>
                  <li><a href="#"> <i class="fas fa-phone p-2"></i> +1 (035) 1234-5678</a></li>
                  <li><a href="#"> <i class="fas fa-envelope p-2"></i> hello@example.com</a></li>
                  <li><a href="#"> <i class="fas fa-map-marker-alt p-2"></i> Main Avenue, 987</a></li>
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

// 06 know
.know-form {
   background-color: $darkest-bg;
   .content {
      @include gs-wrap;
      .textarea, .form {
         width: 50%;
      }
      .subs {
         color: $main-btn;
      }
      h2 {
         color: $main;
      }
      p {
         color: $subtitle;
      }
      input {
         width: 100%;
         background-color: #19191E;
         border: none;
      }
   }  
}

// 07 - form2
.form {
   width: 70%;
   p {
      color: $subtitle;
   }
   .subs {
      color: $main-btn;
   }
   .gs-form, .input-inner {
     width: 48%;
   }
   select, i {
      color: #6C757D;
   }

   textarea, .gs-form {
      border-radius: 2px;
      border: none;
      background-color: #ECECEC;
   }
   textarea {
      resize: none;
   }

   .input-inner {
      position: relative;
      i {
         position: absolute;
         right: 5px;
         top: 10px;
      }
      input {
         width: 100%;
      }
   }

}
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