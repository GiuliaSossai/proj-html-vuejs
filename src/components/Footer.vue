<template>
  <footer>
     <div class="footer-top gs-lgt">
        <div class="gs-wrap">
           <FooterMenu :footerList = "aboutList" />
        </div>
     </div>

     <!-- footer-bottom -->
     <div class="footer-bottom gs-lgt">
        <div class="gs-wrap d-flex justify-content-between align-items-center py-4">
            <p>Enjoy the low price. We are tracking any intention of piracy</p> 
            <p>&copy; 2020 NEXGEN is proudly powered by <span>Codings</span>.</p>
         </div>
     </div>
  </footer>
</template>

<script>
import FooterMenu from './FooterMenu.vue';

export default {
   name: 'Footer',
   components: {
      FooterMenu,   
   },

   data(){
      return {
         aboutList: [
            {
               id: "1",
               name: 'About',
               elements: ['The Company', 'Institutional', 'Social & Events', 'Innovation', 'Environment', 'Technology']
            },

            {
               id: "2",
               name: 'Services',
               elements: ['Audit & Assurance', 'Financial Advisory', 'Analytics M&A', 'Middle Marketing', 'Legal Consulting', 'Regulatory Risk']
            },

            {
               id: "3",
               name: 'Support',
               elements: ['Responsability', 'Terms of Use', 'About Cookies', 'Privacy Policy', 'Accessibility', 'Information']
            }
         ] 
      }
   }
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
   a:hover {
      color: $main;
   }
}

.footer-bottom{
   background-color: $dark-bg;
   p {
      margin: 0;
      font-size: 18px;
      span {
         color: $main-btn;
      }
   }
}

</style>