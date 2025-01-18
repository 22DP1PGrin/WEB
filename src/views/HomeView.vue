<template >
  <Navbar/> 
  <MainInfo/>
  <br><br><br><br><br><br><br><br><br><br>
  <br><br><br><br><br><br><br>
  <BonusInfo/>
  <br><br><br><br><br><br><br><br><br><br><br><br>
  <h2 class="header">Do what you've been wanting for a long time!</h2> <!-- Aicinājums rīkoties -->
  <br>
  <Cards/>
  <br><br><br><br><br><br>
  <Footer/>
  

</template>

<script>
import Navbar from '@/components/Navbar.vue';
import Footer from '@/components/Footer.vue';

export default{
  components: {
    Navbar,
    Footer,
  }
}
</script>

<style scoped>
  .header{
    color:rgba(26, 16, 8, 0.8); /* Teksta krāsa */
    text-align: center; /* Teksta centrēšana */
  }

</style>