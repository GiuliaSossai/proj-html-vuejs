<template>
  <footer>
     <div class="footer-top">
        <div class="container row">
           <div class="col contacts-menu">
               <div class="logo">
                 <img src="../assets/img/nexgen-logo.svg" alt="nexgen-logo">
               </div>
               <p>A Functoinal HTML Template for Corporate & Business.</p>
               <ul>
                  <li><a href="#"> <i class="fas fa-phone"></i> +1 (035) 1234-5678</a></li>
                  <li><a href="#"> <i class="fas fa-envelope"></i> hello@example.com</a></li>
                  <li><a href="#"> <i class="fas fa-map-marker-alt"></i> Main Avenue, 987</a></li>
               </ul>

               <button class="btn gs-btn mt-2">get in touch</button>
            </div>

           <div class="col footer-menu py-4 px-3">
              <h5>About</h5>
              <ul>
                 <li><i class="fas fa-chevron-right"></i><a href=""> aaaa</a></li>  
                 <li><i class="fas fa-chevron-right"></i><a href=""> aaaa</a></li>  
                 <li><i class="fas fa-chevron-right"></i><a href=""> aaaa</a></li>  
                 <li><i class="fas fa-chevron-right"></i><a href=""> aaaa</a></li>  
                 <li><i class="fas fa-chevron-right"></i><a href=""> aaaa</a></li>  
                 <li><i class="fas fa-chevron-right"></i><a href=""> aaaa</a></li>  
              </ul>
            </div>
           <div class="col footer-menu py-4 px-3">
              <h5>Services</h5>
              <ul>
                 <li><i class="fas fa-chevron-right"></i><a href=""> aaaa</a></li>  
                 <li><i class="fas fa-chevron-right"></i><a href=""> aaaa</a></li>  
                 <li><i class="fas fa-chevron-right"></i><a href=""> aaaa</a></li>  
                 <li><i class="fas fa-chevron-right"></i><a href=""> aaaa</a></li>  
                 <li><i class="fas fa-chevron-right"></i><a href=""> aaaa</a></li>  
                 <li><i class="fas fa-chevron-right"></i><a href=""> aaaa</a></li>  
              </ul>
           </div>
           <div class="col footer-menu py-4 px-3">
              <h5>Support</h5>
              <ul>
                 <li><i class="fas fa-chevron-right"></i><a href=""> aaaa</a></li>  
                 <li><i class="fas fa-chevron-right"></i><a href=""> aaaa</a></li>  
                 <li><i class="fas fa-chevron-right"></i><a href=""> aaaa</a></li>  
                 <li><i class="fas fa-chevron-right"></i><a href=""> aaaa</a></li>  
                 <li><i class="fas fa-chevron-right"></i><a href=""> aaaa</a></li>  
                 <li><i class="fas fa-chevron-right"></i><a href=""> aaaa</a></li>  
              </ul>
           </div>
        </div>
     </div>




     <!-- footer-bottom -->
     <div class="footer-bottom">
        <div class="container d-flex justify-content-between align-items-center py-4">
            <p>Enjoy the low price. We are tracking any intention of piracy</p> 
            <p>&copy; 2020 NEXGEN is proudly powered by <span>Codings</span>.</p>
         </div>
     </div>
  </footer>
</template>

<script>
export default {
   name: 'Footer',
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

.footer-top {
   background-image: url('../assets/img/bg-7.jpg');
   min-height: 300px;
   @include bg-position;
   padding: 80px 0;
   color: $subtitle;
   a {   
      color: $subtitle;
      &:hover {
         color: $main;
      }
   }

   .row {
      margin: 0 auto;
      .contacts-menu{
         //background-color: rgb(97, 93, 93);    
         .logo {
            cursor: pointer;
            width: 100px;
         }
         .fas {
            font-size: 14px;
            color: lighten($subtitle, 30%);
         }
      }
      
      .footer-menu {
         margin: 0 15px;
         min-height: 100px;
         background-color: rgba(182, 181, 181, 0.1);
         border-radius: 5px;
         h5 {
            color: $main;
         }
      }
   }
}

.footer-bottom{
   color: $subtitle;
   background-color: $dark-bg;
   p {
      margin: 0;
      span {
         color: $main-btn;
      }
   }
}

</style>