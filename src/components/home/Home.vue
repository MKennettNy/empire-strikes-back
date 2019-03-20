<template>
  <div>
    <div class="landing-collage">
      <img @click="navigateTo('planet')" class="landing-img moon" src="../../../images/moon.png" alt="">
      <!-- <img @click="navigateTo('planet')" class="landing-img dagobah" src="../../../images/planet-dagobah.png" alt=""> -->
      <!-- <img @click="navigateTo('starships')" class="landing-img tie-bomber" src="../../../images/tie-bomber.png" alt=""> -->
      <img @click="navigateTo('character')" class="landing-img darth" src="../../../images/darth-vader.png" alt="">
      <!-- <img @click="navigateTo('character')" class="landing-img leia" src="../../../images/leia.png" alt=""> -->
      <img @click="navigateTo('character')" class="landing-img luke" src="../../../images/luke.png" alt="">
      <!-- <img @click="navigateTo('starships')" class="landing-img r2-d2" src="../../../images/R2-D2.png" alt=""> -->
      <!-- <img @click="navigateTo('character')" class="landing-img c-3po" src="../../../images/C-3PO.png" alt=""> -->
      <!-- <img @click="navigateTo('starships')" class="landing-img y-wing" src="../../../images/y-wing.png" alt=""> -->
      <!-- <img @click="navigateTo('starships')" class="landing-img x-wing" src="../../../images/x-wing.png" alt=""> -->
    </div>
    <Credits />
  </div>
</template>

<script>
import Credits from "./Credits";

export default {
  name: "Home",
  components: {
    Credits
  },
  data: function() {
    return {
   
    };
  },
  methods: {
    navigateTo: function(searchQuery) {
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
.landing-starship {
  /* max-width: 400px; */
  position: absolute;
}
</style>