<template>
  <div class="col footer-menu py-4 px-3">
              <h5>Support</h5>
              <ul>
                 <li
                  v-for="(item, index) in supportList"
                  :key="index"
                 >
                    <i class="fas fa-chevron-right"></i>
                    <a href=""> {{item}}</a>
                  </li>  
              </ul>
   </div>
</template>

<script>
export default {
   name: 'Support',
   props: {
      supportList: Array
   }
}
</script>

<style>

</style>