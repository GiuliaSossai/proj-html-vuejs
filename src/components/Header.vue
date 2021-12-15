<template>
  <header>
      <Contacts />
      <Menu />  
  </header>
</template>

<script>
import Contacts from './Contacts.vue';
import Menu from './Menu.vue';

export default {
   name: 'Header',
   components: {
      Contacts,
      Menu,
   }
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';

header {
   color: $subtitle;
}

</style>