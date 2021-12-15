<template>
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
</template>

<script>
export default {
   name: 'Form'
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';
@import '../assets/style/mixins.scss';

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

</style>