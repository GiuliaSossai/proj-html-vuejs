<template>
  <div class="content d-flex justify-content-between align-items-center">
           <div class="textarea">
               <p class="subs">newsletter</p>
               <h2><span class="special-dark-title px-3 pb-2">Know</span> first</h2>
               <p class="gs-lgt">Follow closely and receive content about our company and the news of the current market</p>
           </div>
           
           <div class="form">
              <input type="text" class="form-control d-block" placeholder="Name" aria-label="Name" aria-describedby="basic-addon1">
              <input type="text" class="form-control d-block my-3" placeholder="Email" aria-label="Email" aria-describedby="basic-addon1">
              <button class="btn gs-solid-btn">subscribe</button>
           </div>
        </div>
</template>

<script>
export default {
   name: 'NewsLetter'
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';
@import '../assets/style/mixins.scss';

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
      height: 50px;
      background-color: #232328;
      border: none;
   }
}

</style>