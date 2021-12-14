<template>
  <main>
     <!-- 01 video -->
     <VideoSection />

     <!-- 02 numbers -->
     <ResultsSection />

     <!-- 03 services -->
     <ServicesSection />

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
import VideoSection from './VideoSection.vue';
import ResultsSection from './ResultsSection.vue';
import ServicesSection from './ServicesSection.vue';

export default {
   name: 'Main',
   components: {
      VideoSection,
      ResultsSection,
      ServicesSection,

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


</style>