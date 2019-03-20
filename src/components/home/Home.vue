<template>
  <div>
    <div class="landing-collage">
      <img @click="navigateTo('detail')" class="landing-planet" src="../../../images/moon.png" alt="">
      <img @click="navigateTo('detail')" class="landing-character" src="../../../images/darth-vader.png" alt="">
      <img @click="navigateTo('detail')" class="landing-starship" src="../../../images/tie-bomber.png" alt="">
      <img @click="navigateTo('detail')" class="landing-character" src="../../../images/C-3PO.png" alt="">
      <img @click="navigateTo('detail')" class="landing-character" src="../../../images/luke.png" alt="">
      <img @click="navigateTo('detail')" class="landing-planet" src="../../../images/planet-dagobah.png" alt="">
      <img @click="navigateTo('detail')" class="landing-starship" src="../../../images/R2-D2.png" alt="">
      <img @click="navigateTo('detail')" class="landing-character" src="../../../images/leia.png" alt="">
      <img @click="navigateTo('detail')" class="landing-starship" src="../../../images/y-wing.png" alt="">
      <img @click="navigateTo('detail')" class="landing-starship" src="../../../images/x-wing.png" alt="">
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  data: function() {
    return {
   
    };
  },
  methods: {
    navigateTo: function(Detail) {
      this.$router.push({ name: "detail", params: { searchQuery: searchQuery } });
    }
  },
  created: function() {
   
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.landing-planet, 
.landing-character, 
.landing-starship 
  { max-width: 400px; }
</style>