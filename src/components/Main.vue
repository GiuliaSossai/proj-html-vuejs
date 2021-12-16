<template>
  <main>
     <!-- 01 video -->
     <section class="gs-wrap">
         <div class="contents text-center">
            <p class="subs">introduction video</p>
            <h2>Advisory <span class="special-title px-3 pb-2">Performance</span></h2>
            <p class="text mb-5">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Minus fugit, quisquam voluptate optio labore exercitationem, sequi vero incidunt unde laudantium sapiente excepturi aperiam.</p>

            <Video />
         </div>   
      </section>
     

     <!-- 02 numbers -->
     <section class="results-bg">
         <div class="contents text-center">
            <p class="subs">what are we doing</p>
            <h2><span class="special-dark-title px-3 pb-2">Results</span> in Numbers</h2>
         </div>

         <div class="gs-wrap row text-center">
            <div class="col"
               v-for="(item, index) in Results"
               :key="index"
            >
               <h4 class="gs-grn">{{item.quantity}}</h4>
               <h5>{{item.text}}</h5>
            </div>
         </div>
      </section>

     <!-- 03 services -->
     <section class="services-section">
         <div class="gs-wrap">
            <p class="subs">our business area</p>
            <h2>Excellence in <span class="special-dark-title px-3 pb-2">Services</span></h2>

            <div class="d-flex justify-content-between align-items-center">
               <p class="gs-lgt text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Minus fugit, quisquam voluptate optio labore exercitationem</p>
                  
               <button class="btn gs-btn">see all</button>
            </div>
               
            <BoxesList />   
         </div>  
      </section>

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

            <Quote />
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

     <!-- 07 form -->
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
                     <a href="#" class="gs-grn">
                        <i :class="contact.icon.join(' ')" class="p-2"></i>
                        {{contact.text}} 
                     </a>   
                  </li>
               </ul>
               <button class="btn gs-btn mt-3 gs-grn">view map</button>
           </div>
        </div>
     </section>
  </main>
</template>

<script>
import Video from './Video.vue'; //componente 01
import BoxesList from './BoxesList.vue'; //componente 03
import CardsList from './CardsList.vue'; // componente 04
import Quote from './Quote.vue'; // componente 04
import EditorialContent from './EditorialContent.vue'; // componente 05
import NewsLetter from './NewsLetter.vue'; // componente 06
import Form from './Form.vue'; // componente 07

//database js
import Results from "../assets/data/Results.js";
import ContactsSmall from "../assets/data/ContactsSmall.js";

export default {
   name: 'Main',
   components: {
      Video,
      BoxesList,
      CardsList,
      Quote,
      EditorialContent,
      NewsLetter,
      Form
   },
   data(){
      return {
         Results,
         ContactsSmall,
         //counter: 0
      }
   },
   methods: {
      //funzione per visualizzare un'animazione dei numeri nella sezione 02 al mounted della pagina
      getResults(){
         let counter = 0;
         console.log(counter);
         console.log(this.Results[0].quantity);
         
         // const clock = setInterval(function(){
         //    counter++;
         //    console.log('incremento counter', counter++);
         //    if(counter == 10){
         //       clearTimeout(clock);
         //       this.Results[0].quantity = 10;
         //    }
         // },100)
      }
   },
   mounted(){
      this.getResults();
   }

}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';
@import '../assets/style/mixins.scss';

//01 video
.contents {
   @include gs-wrap;
   .text{
      color: $subtitle;
   }
}

//02 numbers
.results-bg {
   background-image: url('../assets/img/bg-1.jpg');
   @include bg-position;
   h2, h5{
      color: $main;
   }
   .row {
      margin: 30px auto;
      h4 {
         font-size: 32px;
      }
      h5 {
         font-size: 25px;
      } 
   }  
}

//03 services
.services-section {
   background-color: $darkest-bg;
   color: $main;
   .text {
      width: 70%;
   }
}


// 04 team
.textarea {
   width: 60%;
   .text {
      color: $subtitle;
   }
}

// 05 news
.news {
   background-color: $light-green;
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
}

</style>