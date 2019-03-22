<template>
  <div class="container">
      <h2>Name: {{ contentdata.name }}</h2>
      <!-- <img src="" alt=""> -->
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
      text-shadow: 0 0 25px pink, 0 0 5px hotpink;
      font-size: 50px;
    }
    .content{
      background-color: #222;
      background-image: url("https://www.transparenttextures.com/patterns/old-moon.png");
    }
</style>
