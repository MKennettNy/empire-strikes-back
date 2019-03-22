<<template>
 <div class="container">
     
      <div class="data" v-for="(value, key) in contentdata">
       {{ key }} : {{ value }}       
      </div>
 </div>
</template>

<script>
  export default {
    name: "Content",
    props: ["contentdata"],
    watch: {
      contentdata: function(val) {
        this.contentdata=val;
      }
    }
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h2{
      color: white;
      text-shadow: 0 0 25px black, 0 0 5px black;
      font-size: 50px;
    }
    .content{
      background-color: #222;
      background-image: url("https://www.transparenttextures.com/patterns/old-moon.png");
    }

    /* .starship, .planets, .people {
      padding: 20px;
    } */
</style>
